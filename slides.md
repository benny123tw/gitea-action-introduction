---
theme: academic
title: "Gitea Actions Introduction"
info: |
  ## Gitea Actions Introduction
  Write your first action!
drawings:
  persist: false
transition: slide-left
fonts:
  sans: Montserrat, Roboto Mono, Roboto Slab
mdc: true
colorSchema: light
highlighter: shiki

hideInToc: true
layout: cover

coverAuthor: Benny Yen
coverAuthorUrl: https://github.com/benny123tw
coverBackgroundUrl: https://images.unsplash.com/photo-1521017432531-fbd92d768814?q=80&w=2340&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
class: text-white
---

<v-switch>
  <template #0>
    <h1>GitHub Actions</h1>
  </template>
  <template #1>
  <h1>
    <StrikeThroughText>GitHub</StrikeThroughText>
    Actions
  </h1>
  </template>
  <template #2>
    <div
      v-motion
      :initial="{ x: -80 }"
      :click-2="{ x: 0, y: 40 }"
    ><h1 text-green>Gitea</h1></div>
    <h1>
      <StrikeThroughText :animate=false>GitHub</StrikeThroughText>
      Actions
    </h1>
  </template>
</v-switch>

## Write your first action!

<Pagination classNames="text-gray-300" />

---
src: ./pages/goals.md
---

---
src: ./pages/github-actions.md
---

---
src: ./pages/gitea-actions.md
---

---
src: ./pages/how-to-read-an-action.md
---
