# Deployment guide

This page walks through deploying the full VoiceConnect stack into your own
Azure subscription. The deployment is fully scripted by
[`../src/infra/deploy.ps1`](../src/infra/deploy.ps1) — this guide explains
what the script does and what you'll need before running it.

## Prerequisites

- An **Azure subscription** with the following quotas in the listed regions:
  - Sweden Central — quota for **Consumption-GPU-NC8as-T4** and
    **Consumption-GPU-NC24-A100** workload profiles in Azure Container Apps.
  - West Central US — quota for an **Azure Container Apps Express
    environment**.
- The **Azure CLI** with the `containerapp` extension. The deploy script
  will install the extension automatically if it is missing.
- **PowerShell 7+** (the deploy script uses PowerShell-only syntax).
- **GitHub CLI** (only if you want to clone via `gh repo clone`).
- A **Twilio account** with a phone number, if you want to exercise the
  phone path. The browser path works without Twilio.

## What gets provisioned

| Resource | Region | Purpose |
|---|---|---|
| Resource group `ORB-connect-9` | Sweden Central | Standard Azure Container Apps environment |
| Resource group `ORB-connect-express-9` | West Central US | Express environment |
| Azure Container Registry | Sweden Central | Built images for all seven services |
| User-assigned managed identity | Sweden Central | ACR pull, Application Insights ingestion |
| Log Analytics workspace `orbconnect-law` | Sweden Central | Single sink for everything |
| Application Insights | Sweden Central | Auto-instrumented telemetry for all seven apps |
| ACA managed environment (standard) | Sweden Central | Hosts server, STT, TTS, SRE adapter, sandbox pool |
| ACA managed environment (Express) | West Central US | Hosts Aria, Nova, Twilio bridge |
| Session pool | Sweden Central | Per-agent sandboxes for Aria and Nova |
| 7 Azure Container Apps | Sweden + West Central US | The actual services |

## One-shot deploy

```powershell
gh repo clone simonjj/voiceconnect
cd voiceconnect/infra
./deploy.ps1 -SubscriptionId <your-sub-id>
```

The script is idempotent and re-runnable. On a second run it will skip
provisioning steps that have already completed and only rebuild and roll
the container images that have changed.

### Useful flags

| Flag | Effect |
|---|---|
| `-SkipBuild` | Re-deploy bicep but do not rebuild any container images |
| `-SkipDeploy` | Build images but do not run the bicep deployments |
| `-AppInsightsConnectionString <conn>` | Reuse an existing Application Insights instance instead of looking up the default one |
| `-AppInsightsName <name> -AppInsightsResourceGroup <rg>` | Look up the connection string for an Application Insights instance you already own |

## After deploy

The script prints the browser client URL at the end. Open it, allow
microphone access, and start talking — Aria responds in a green theme,
Nova in a magenta one. Say "hey Aria, …" or "hey Nova, …" to address a
specific persona.

To wire up the phone path, point a Twilio phone number's voice webhook at
`https://<twilio-bridge-fqdn>/voice` (the FQDN is also printed at the end
of the deploy).

## Tearing down

```powershell
az group delete -n ORB-connect-9 --yes --no-wait
az group delete -n ORB-connect-express-9 --yes --no-wait
```

Both resource groups can be deleted in any order; there are no cross-RG
dependencies that block deletion.
