---
layout: center
---

#### How to read an action?

---
layout: two-cols
---

#### All starts with a `action.yml` file

```yaml {*|15-20}
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
