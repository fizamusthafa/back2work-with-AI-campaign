---
layout: default
title: Home
nav_order: 1
permalink: /
---

# Back to Work Agent — Setup & Deployment

This documentation guides you through the deployment possibilities of the **Back to Work** agent. Choose the flavour which best fits your organization's demands and possibilities. There is a clear recommendation to use **Option 3** for maximized impact, organizational activation and active participation.

This agent is part of the community project **"Back to Work Campaign"**, which additionally consists of a ready-to-use Learning Path and campaign assets. For the full overview and to make your campaign most successful, check out all contents on the [GitHub repository](https://github.com/JaysonBucket/back2work-with-AI-campaign).

---

## Deployment Options

<div class="option-cards">

<div class="option-card blue">
<h3>1 — Easy & Free</h3>

<p>The easiest setup option — follow the instructions on GitHub. Set up in Agent Builder.</p>

<ul>
<li><a href="https://github.com/JaysonBucket/back2work-with-AI-campaign">Source on GitHub</a></li>
<li>Set up in 3 minutes</li>
<li><strong>Positive:</strong> Solely declarative and web-grounded. Usable by everyone without any cost. No pay-as-you-go.</li>
<li><strong>Downside:</strong> The agent has to be shared and the link distributed. Not findable in the agent library.</li>
<li><strong>Manual action:</strong> Users open the agent, install it, and pin it (three ellipses) to find it every day.</li>
</ul>
</div>

<div class="option-card green">
<h3>2 — Max Visibility, Centrally Deployed</h3>

<ul>
<li>Create as a declarative agent in Copilot Studio (<a href="01-import-solution">instructions in this document</a>)</li>
<li>Publish to the org agent library</li>
<li>Deploy and pin centrally to every user</li>
</ul>

<p><strong>Positive:</strong> Centrally managed and pinned. No one has to manually click or pin. Maximum distribution.</p>
<p><strong>Cost:</strong> Solely declarative and web-grounded. Users with Copilot Chat (free) use it with minimal cost via pay-as-you-go. Users with M365 Copilot license use it for free.</p>
</div>

<div class="option-card orange">
<h3>3 — Max Impact with Daily Nudges ⭐ Recommended</h3>

<ul>
<li>Create as a declarative agent in Copilot Studio</li>
<li>Add a daily triggered action to actively reach out to users</li>
<li>Publish to the org agent library</li>
<li>Deploy and pin centrally to every user</li>
</ul>

<p><strong>Positive:</strong> Maximum impact and active trigger to users. Ensures use and awareness every single day.</p>
<p><strong>Cost:</strong> Same as Option 2 plus consumption-based cost for trigger usage.</p>
</div>

</div>

---

## Built With

This solution leverages the following Microsoft SDKs and technologies:

### Microsoft 365 Agents SDK
A comprehensive framework for building full-stack, multi-channel AI agents that operate seamlessly across Microsoft 365 Copilot, Teams, and custom applications. Provides enterprise-grade identity, security, and governance for agent development.

[Learn more →](https://learn.microsoft.com/en-us/microsoft-365/agents-sdk/)

### Agent 365 SDK and CLI
Purpose-built tools for extending agents with enterprise features including identity management, security, observability, and governed access to Microsoft 365 data. The CLI automates the development lifecycle from setup to deployment.

[Learn more →](https://learn.microsoft.com/en-us/microsoft-agent-365/developer/)

### Microsoft Foundry SDK
Unified access to AI models, agents, and tools for building intelligent applications at scale. Supports Python, C#, Java, and JavaScript/TypeScript with comprehensive authentication and deployment capabilities.

[Learn more →](https://learn.microsoft.com/en-us/azure/ai-foundry/)

### Power Apps SDK
Developer tools and APIs for building and extending Power Platform applications, including custom connectors, component frameworks, and integration with Dataverse for enterprise data management.

[Learn more →](https://learn.microsoft.com/en-us/power-platform/developer/)

---

## Documentation Sections

Follow these steps in order to deploy the agent:

| Step | Section | Description |
|------|---------|-------------|
| 1 | [Import Solution](01-import-solution) | Download and import the agent solution into Copilot Studio |
| 2 | [Publish Agent](02-publish-agent) | Test, configure, and publish the agent to your organization |
| 3 | [Admin Deploy & Pin](03-admin-deploy-pin) | Administrator approval, deployment, and pinning in M365 Copilot |
| 4 | [Deploy & Pin in Teams](04-deploy-pin-teams) | Deploy and pin the agent in Microsoft Teams |
| 5 | [Daily Nudge Setup](05-daily-nudge) | Configure the Power Automate flow for daily proactive outreach |
