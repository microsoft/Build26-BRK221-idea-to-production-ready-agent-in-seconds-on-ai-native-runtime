# 🚀 Get Started

**This repo is where attendees go to continue their learning after your session — and your Copilot agent will help you set it up.**

### Step 1: Open your repo

Open this repo in a **Codespace** (click the green **Code** button → **Create a Codespace**) — or clone it locally. Then open **GitHub Copilot Chat**.

### Step 2: Add your content

Give the agent something to work with. Drag files into the Explorer panel — session abstracts, outlines, screenshots, notes — and drop them in one of two places:

| Where to put it | What goes there | Who sees it |
|---|---|---|
| **`_remove-before-publish/`** | Internal reference materials (abstracts, outlines, screenshots, planning docs) | **Copilot only** — never published |
| **`/docs/`, `/src/`, or repo root** | Lab instructions, demo code, sample data, getting-started guides | **Attendees** — published with the repo |

> 💡 Not sure? Start by dropping your session abstract or outline into `_remove-before-publish/`. The agent will figure out what to do with it.

### Step 3: Ask the Agent

Once your content is in the repo, use these three phrases with Copilot to build out your session repo:

| Phrase to use with Copilot | What it does | When to run it |
|---|---|---|
| **"Help me get started"** | Sets up session title, description, outcomes, and owners | After you've added your session abstract or outline to the repo |
| **"Help me refine content"** | Organizes your session content into the repo | Each time you add or update content |
| **"Help me finalize"** | Final review, cleanup, and publication prep | When you're ready to publish |

> 💡 **These three phrases are just the starting point.** Copilot can do much more — try asking it to brainstorm next steps for attendees, generate code samples, or build out your repo structure. Don't be afraid to put it in plan mode and ask for what you need.

---

<a name="start-building"></a>
<br>
<p align="center">
<img src="img/banner-build-26.png" alt="Microsoft Build 2026" width="1200"/>
</p>

# [Microsoft Build 2026](https://build.microsoft.com)

## 🔥 BRK221: Idea to production-ready agent in seconds on AI-native runtime

### Session Description

Agentic workloads demand a fundamentally different runtime than traditional app hosting. In this breakout you'll see why, and how Azure Container Apps delivers the speed, isolation, and scale needed to run production-ready agents — including sandboxes, MCP tools, and serverless GPUs. We pair a live end-to-end demo with a customer story so you walk away with patterns and resources to go from idea to deployed agent in seconds, on an AI-native runtime you can trust in production.

### 🚀 Getting started

If you're following these steps at your own pace:
- Clone this repository
- Set up your development environment
- <!-- step 3 -->

### 🧠 Learning Outcomes

By the end of this session, you will be able to:

- Explain why agentic workloads demand a fundamentally different runtime than traditional app hosting, and the key challenges teams face taking agents to production.
- Describe how Azure Container Apps delivers the speed, isolation, and scale needed to run production-ready agents — including sandboxes, Model Context Protocol tools, and serverless GPUs.
- Apply patterns and resources to go from idea to deployed agent in seconds on an AI-native runtime you can trust in production.

### 💬 Keep Learning with Copilot

Try these prompts with GitHub Copilot to explore the topics from this session. Open Copilot Chat in VS Code (`Ctrl+Alt+I` on Windows/Linux, `Cmd+Shift+I` on Mac), paste a prompt, and see what you learn. Try connecting the [Microsoft Learn MCP Server](#-microsoft-learn-mcp-server) for the latest official documentation.

Use these as a starting point — or write your own!

<!-- Prompts will be tailored to this session's content during repo setup. -->

> *Prompts coming soon — check back after the session content is finalized.*

### 💻 Technologies Used

1. [Azure Container Apps](https://learn.microsoft.com/azure/container-apps/overview)
1. [Azure Container Apps Sandboxes (Session Pools)](https://learn.microsoft.com/azure/container-apps/sessions)
1. [Serverless GPUs in Azure Container Apps](https://learn.microsoft.com/azure/container-apps/gpu-serverless-overview)
1. [Azure Container Apps Express environment](https://learn.microsoft.com/azure/container-apps/environment)
1. [Twilio ConversationRelay](https://www.twilio.com/docs/voice/twiml/connect/conversationrelay)
1. [GitHub Copilot CLI](https://docs.github.com/copilot/github-copilot-in-the-cli/about-github-copilot-in-the-cli)
1. [Azure Application Insights](https://learn.microsoft.com/azure/azure-monitor/app/app-insights-overview)
1. [Bicep](https://learn.microsoft.com/azure/azure-resource-manager/bicep/overview)

### 📚 Resources and Next Steps

| Resource | Description |
|:---------|:------------|
| [https://aka.ms/build26-next-steps](https://aka.ms/build26-next-steps) | Explore lab and session repos to further your learning from Microsoft Build |


### 🌟 Microsoft Learn MCP Server

The Microsoft Learn MCP Server gives your AI agent direct access to Microsoft's official documentation — grounded, up-to-date answers about the products and services covered in this session.

**VS Code** — One click installation: 

[![Install in VS Code](https://img.shields.io/badge/VS_Code-Install_Microsoft_Learn_MCP-0098FF?style=flat-square&logo=visualstudiocode&logoColor=white)](https://vscode.dev/redirect/mcp/install?name=microsoft-learn&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Flearn.microsoft.com%2Fapi%2Fmcp%22%7D)


**GitHub Copilot CLI** — Run this to install the Learn MCP Server as a plugin:
```
/plugin install microsoftdocs/mcp
```

For more info, other clients, and to post questions, visit the [Learn MCP Server repo](https://aka.ms/learnmcp).

## Content Owners

<table>
<tr>
    <td align="center"><a href="http://github.com/devanshidiaries">
        <img src="https://github.com/devanshidiaries.png" width="100px;" alt="Devanshi Joshi"/><br />
        <sub><b>Devanshi Joshi</b></sub></a><br />
            <a href="https://github.com/devanshidiaries" title="talk">📢</a>
    </td>
    <td align="center"><a href="http://github.com/simonjj">
        <img src="https://github.com/simonjj.png" width="100px;" alt="Simon Jakesch"/><br />
        <sub><b>Simon Jakesch</b></sub></a><br />
            <a href="https://github.com/simonjj" title="talk">📢</a>
    </td>
</tr></table>

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit [Contributor License Agreements](https://cla.opensource.microsoft.com).

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft
trademarks or logos is subject to and must follow
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.
