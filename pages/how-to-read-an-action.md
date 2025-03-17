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

::left::

# `action.yml`

```yaml {*|1-3|5-9|11-13|15-20}{lines: true}
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

# Workflow

````md magic-move {at: 1, lines: true}

```yaml
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
        with:
          node-version: '20'
          cache: 'pnpm'
```
````