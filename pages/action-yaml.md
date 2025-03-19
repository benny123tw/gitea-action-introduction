---
layout: center
---

# How to write your first action?

---
layout: center
---

## It all starts with a `action.yml` file

---
layout: two-cols-enhanced
---

# `action.yml`

```yaml {*|1-3}{lines: true}
name: Some Action
description: A description of the action
author: Author Name

inputs:
  input1:
    description: Description of input1
    required: true
    default: default value

outputs:
  output1:
    description: Description of output1

runs:
  using: docker
  image: docker-image
  args:
    - arg1
    - arg2
```

---
layout: figure
transition: slide-right
figureCaption: "Screenshot of the marketplace"
figureUrl: /marketplace.png
---

# Marketplace

---
layout: two-cols-enhanced
---

# `action.yml`

```yaml {*|5-9|11-13|15-20}{lines: true}
name: Some Action
description: A description of the action
author: Author Name

inputs:
  input1:
    description: Description of input1
    required: true
    default: default value

outputs:
  output1:
    description: Description of output1

runs:
  using: docker
  image: docker-image
  args:
    - arg1
    - arg2
```

::right::

<h1>Workflow</h1>

```yaml {*|11-12,16-18|15,20|*}{at: 1, lines: true}
name: Test
on:
  push:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
        with:
          fetch-depth: 0

      - uses: actions/setup-node@v4
        id: node
        with:
          node-version: '20'
          cache: 'pnpm'

      - run: echo "${{ steps.node.outputs.node-version }}" 
```

---
layout: two-cols-enhanced
---

# Types of actions

<v-clicks>

- Docker
- JavaScript
- Composite
- Go (Only on <span color-green>Gitea</span>)

</v-clicks>

::right::

<v-switch at="1">

<template #1>

<h1>Docker Example</h1>

<code>entrypoint.sh</code>

```sh
#!/bin/bash
echo "Hello, ${INPUT_WHO_TO_GREET}!"
```

<code>Dockerfile</code>

```dockerfile
FROM ubuntu:latest
COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
```

<code>action.yml</code>

```yaml
runs:
  using: 'docker'
  image: 'Dockerfile'
```

More details: [Creating a Docker container action](https://docs.github.com/en/actions/sharing-automations/creating-actions/creating-a-docker-container-action)

Example: [appleboy/jira-action](https://github.com/appleboy/jira-action)

</template>

<template #2>

<h1>JavaScript Example</h1>

<code>index.js</code>

```js
const core = require('@actions/core');
const github = require('@actions/github');

try {
  // `who-to-greet` input defined in action metadata file
  const nameToGreet = core.getInput('who-to-greet');
  core.info(`Hello ${nameToGreet}!`);
} catch (error) {
  core.setFailed(error.message);
}
```

<code>action.yml</code>

```yaml
runs:
  using: 'node16'
  entrypoint: 'index.js'
```

More details: [Creating a JavaScript action](https://docs.github.com/en/actions/sharing-automations/creating-actions/creating-a-javascript-action)

Example: [actions/checkout](https://github.com/actions/checkout)

</template>

<template #3>

<h1>Composite Example</h1>

<code>action.yml</code>

```yaml
inputs:
  who-to-greet:
    description: 'Who to greet'
    required: true
    default: 'World'

runs:
  using: 'composite'
  steps:
    - name: Checkout
      uses: actions/checkout@v4

    - name: Run a step
      run: echo "Hello, ${INPUT_WHO_TO_GREET}!"
```

More details: [Creating a composite action](https://docs.github.com/en/actions/sharing-automations/creating-actions/creating-a-composite-action)

Example: [reviewdog/action-eslint](https://github.com/reviewdog/action-eslint)

</template>

<template #4>

<h1>Go Example</h1>

<code>main.go</code>

```go
package main

import (
  gha "github.com/sethvargo/go-githubactions"
)

func main() {
  fmt.Printf("Hello, %s!", gha.GetInput("who-to-greet"))
}
```

<code>action.yml</code>

```yaml
runs:
  using: 'go'
  main: 'main.go'
```

More details: [Creating a Go action](https://blog.gitea.com/creating-go-actions/)

Example: [Zettat123/simple-go-action](https://gitea.com/Zettat123/simple-go-action)

</template>
</v-switch>
