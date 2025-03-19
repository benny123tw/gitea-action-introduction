---
layout: two-cols
---

<ul text-3xl>
  <li>Workflows</li>
  <li v-click="'+1'"><a href="https://docs.github.com/en/actions/writing-workflows/choosing-when-your-workflow-runs/events-that-trigger-workflows">Events</a></li>
  <li v-click="'+1'">Jobs</li>
  <li v-click="'+1'">Actions</li>
  <li v-click="'+1'">Runners</li>
</ul>

::right::

````md magic-move {at:1, lines: true}
Workflows

```yaml {*|3-5}
name: Deploy pages

on:
  push:
    branches: [main]

permissions:
  contents: read
  pages: write

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v4

      - uses: actions/setup-node@v4
        with:
          node-version: 'lts/*'

      - uses: pnpm/action-setup@v2
        with:
          run_install:
            - --frozen-lockfile
# ...
```

Events

```yaml {3-5}
name: Release

on:
  tag:
    - v*

jobs:
  release:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v4

      - uses: actions/setup-node@v4
        with:
          node-version: 'lts/*'

      - uses: pnpm/action-setup@v2
        with:
          run_install:
            - --frozen-lockfile
# ...
```

Jobs

```yaml
# ...
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - uses: actions/setup-node@v4
        with:
          node-version: 'lts/*'

      - uses: pnpm/action-setup@v2
        with:
          run_install:
            - --frozen-lockfile
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    needs: build
    runs-on: ubuntu-latest
    name: Deploy
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```
````