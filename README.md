# eDKP 2026 Guide

## Table of Contents
- [Requirements](#requirements)
- [Constraints](#constraints)
- [Setup](#setup)
- [Recommended Stacks](#recommended-stacks)
- [Delieverables](#deliverables)
- [Best Practices](#best-practices)

## General Information
Welcome to the eDKP 2026 hackathon.  
This guide will help you get up and running quickly so you can get started hacking.

## Requirements
1. All participants will be provided a laptop capable of internet connection, installation of packages, access to Kiro IDE ([link](https://kiro.dev)) and access to Github ([link](https://github.com/)).
2. If your use case requires data/access to models, please bring either of the following:  
i. Prepare (eg. mask / anonymise) and bring your own data.  
ii. If you need news data or access to open source models, inform us and we will provide you with a Tavily API key or HuggingFace API key. ([ref](#3-tavily-for-news-related-team-only))

## Constraints
1. Maximum usage of $500 credits per team on AWS Innovation Sandbox (All AWS Services will be available)

New: With the support of AWS Innovation Sandbox, this year, teams have access to DB services and GPUs.

## Setup
Follow the setup steps in this order:
### 1. Github
Github is a platform to share code for collaborative development.  
Your team repositories have been prepared for you beforehand. Check that you are able to access it using the steps below:
1. Create your Github account by following the registration instructions on their sign-up page. ([link](https://github.com/signup?source=login))  
3. Provide the Tech Facilitators with your Github username / email. We have to grant you access to the eDKP2026 Github resources.
4. After obtaining access, go to the eDKP2026 Github page. ([link](https://github.com/edkp-hackathons/))
5. Sign in with your login credentials.
6. A Github repository has been created for each of your teams:  
<img src="assets/images/readme-github-repo1.png">  
7. Click into your team's repository. It should be completely empty.  
8. We encourage you to rename your repository. Click onto the 'Settings' tab, thereafter change the value in the text field:  
<img src="assets/images/readme-github-repo2.png">  
9. Create different feature branches per member (this helps to manage conflicts when writing to the same files):   
i. Click on the drop-down under your repository's name that either has 'main' / 'master' (this is your branch selector).  
ii. Type the name of your new branch to create it.  
<img src="assets/images/readme-bestpractices-github.png">  

> ⚠️ **DO NOT** create more than 1 repo per team  

> ℹ️ For information on how your team should use Github for collaboration, please refer [here](#best-practices)

### 2. Kiro and AWS Innovation Sandbox
- ‘Vibe-coding’ platform with a chat interface - Supported with IDE, Cli, Web
- Tightly integrated with Github for easy commits & version tracking
- Tightly integrated with AWS Sandbox for easy deployment

- Each team will be provided with an AWS Sandbox of up to $500 limit
- If the demo requires AWS Bedrock, it can be provisioned in the sandbox
- If the demo requires a Vector / Database, it can be provisioned in the sandbox

### 3. Tavily & Hugging Face APIs

For teams that require **web search** or **AI/ML models**, you may use the following APIs:

#### Tavily — For news-related teams

[Tavily](https://tavily.com/) provides web search and content extraction capabilities designed for LLM applications.

- You can create a **Free Tier** account with **1,000 credits** to get started.
- If you use up your credits, please reach out to your facilitator for an API key.
- For API usage and integration instructions, refer to the official [Tavily API documentation](https://docs.tavily.com/documentation/api-reference/endpoint/search).

#### Hugging Face — For AI/ML models

[Hugging Face](https://huggingface.co/) provides access to a wide range of open-source AI/ML models through its APIs.

- You can create a **free Hugging Face account** and generate an API token.
- Use the API to access supported models for tasks such as text generation, embeddings, classification, and other AI/ML workloads.
- For API usage and integration instructions, refer to the official [Hugging Face API documentation](https://huggingface.co/docs/api-inference/index).
- Keep your API token **private** and do not commit it to your GitHub repository.


## Recommended Stacks
1. Python: FastAPI backend + Streamlit frontend 
2. Javascript: Next.js
> ⚠️ Javascript may not have all the same ML / NLP libraries in Python.  

## Deliverables

1. **Final presentation deck** with:
   - A clear problem statement
   - Business use case
   - Supporting material

2. **A working app** that is deployed to the AWS Innovation Sandbox and runs successfully.
   - **Demonstrate live key features** — show the main functions, even if not all features are fully polished.
   - **Documented and reproducible** — others should be able to run your solution by following the documentation in your codebase.
   - 🥳 **Bonus:** Measurement of LLM evaluation metrics and user feedback.


## Best Practices
### Collaborating using Github
- Typically a team using Github would create a main branch to host stable / tested code, whilst team members can concurrently develop on feature branches. This enables version control when merging code with conflicts (think of writing over the same sentence in a shared Word .docx).
- When working on a feature, the Git / Github workflow should look something like this (🟠 for action taken using Git, 🔵 for GitHub):
    ```mermaid
    graph LR
        A[main branch] --> B[git checkout -b feature-branch]
        B --> C[Make code changes]
        C --> D[git add .]
        D --> E["git commit -m 'message'"]
        E --> F[git push origin feature-branch]
        F --> G[Create Pull Request]
        G --> H[Code Review]
        H --> I[Merge Pull Request]

        classDef git fill:#f96,stroke:#333,stroke-width:2px
        classDef github fill:#6cf,stroke:#333,stroke-width:2px

        class A,B,C,D,E,F,K,L git
        class G,H,I,J github
    ```

> ⚠️ Do get your teammates to review your code before merging the pull request!

> ℹ️ For information on the typical Git + Github workflow, please refer to the this tutorial [video](https://www.youtube.com/watch?v=nCKdihvneS0).

### Spec-Drive Development using 👐 AWS Kiro IDE
> ## Documentation Index
> Fetch the complete documentation index at: https://kiro.dev/llms.txt
> Use this file to discover all available pages before exploring further.

#### IDE

> Features unique to the Kiro desktop IDE — editor, specs, chat, and inline completions

The Kiro IDE is a desktop development environment built on a VS Code foundation, enhanced with agentic capabilities. This section covers the features that are unique to the desktop IDE experience.

  [Video](https://kiro.dev/videos/kiro_1.mp4)

#### IDE-unique features

  - [Editor](https://kiro.dev/docs/ide/editor/interface.md) — Interface layout, keyboard shortcuts, codebase indexing, source control, and extensions.
  - [Specs](https://kiro.dev/docs/specs.md) — Plan and build features using structured specifications with requirements, design, and tasks.
  - [Chat](https://kiro.dev/docs/ide/chat.md) — Interact with your code through natural language conversations with full project context.

#### Features

The IDE shares Kiro's core agent engine with CLI and Web. These capabilities work the same way across all surfaces:

  - [Steering](https://kiro.dev/docs/steering.md) — Guide AI behavior with custom rules and context.
  - [Hooks](https://kiro.dev/docs/hooks.md) — Automate repetitive tasks with intelligent triggers.
  - [MCP Servers](https://kiro.dev/docs/mcp.md) — Connect external tools and data sources.
  - [Custom Agents](https://kiro.dev/docs/custom-agents.md) — Create specialized agents for targeted workflows.
  - [Skills](https://kiro.dev/docs/skills.md) — Extend agent knowledge with domain-specific skills.
  - [Powers](https://kiro.dev/docs/powers.md) — Add capabilities through community packages.

#### Get started

New to Kiro? Start here:

  - [Download & Install](https://kiro.dev/docs/getting-started/installation.md) — Get Kiro running on your machine.
  - [First Project](https://kiro.dev/docs/getting-started/first-project.md) — Learn Kiro's features through a hands-on project.
