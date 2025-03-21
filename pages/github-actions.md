---
layout: center
transition: slide-left
---

# What is GitHub Actions?

<!--
  GitHub Actions is a CI/CD service that makes it easy to automate all your software workflows.
  GitHub Actions was first announced in October 2018 at the GitHub Universe conference (beta release)
-->

---
layout: image
---

![GitHub Actions](/github-action.webp)

<!--
  In November 2019, GitHub Actions became generally available (GA), introducing matrix builds, live logs, and an ecosystem of shared actions.

  By GA, over 1,200 community-created Actions were on the Marketplace. GitHub also added features like self-hosted runners, artifact caching, and support for Linux, macOS, Windows, and ARM builds​

  [New from Universe 2019](https://github.blog/news-insights/product-news/universe-day-one/#:~:text=Today%2C%20we%E2%80%99re%20announcing%20the%20general,this%20list%20is%20growing%20fast)
-->

---
layout: section
transition: fade
---

# How to Use GitHub Actions

- Workflows are defined in `.github/workflows/*.yml`
- YAML-based configuration
- Event-driven automation
- Example events:
  - `push`
  - `pull_request`
  - `schedule`
  - `workflow_dispatch`

---
layout: figure
figureUrl: /github-action-workflow.png
figureCaption: "Screenshot of mastra-ai"
---

# GitHub Actions Workflow

---
layout: center
---

# Run GitHub Actions locally
https://github.com/nektos/act

Testing workflows locally saves time and resources compared to pushing changes repeatedly.

---
layout: full
---

<div class="flex justify-center">
  <video controls class="w-3/4" autoplay muted>
    <source src="/run-workflow-locally.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

---
layout: center
transition: fade
---

# Similar to Gitea Actions

The way we test GitHub Actions locally is very similar to how Gitea Actions works behind the scenes.

---
layout: figure
figureCaption: "Screenshot of gitea/act"
figureUrl: /gitea-action.png
---

# Gitea Actions
