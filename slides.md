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
src: ./pages/action-yaml.md
---

---
layout: two-cols
---

<div class="w-60 relative">
  <div class="relative w-40 h-40">
    <img
      v-motion
      :initial="{ x: 800, y: -100, scale: 1.5, rotate: -50 }"
      :enter="final"
      class="absolute inset-0"
      src="https://sli.dev/logo-square.png"
      alt=""
    />
    <img
      v-motion
      :initial="{ y: 500, x: -100, scale: 2 }"
      :enter="final"
      class="absolute inset-0"
      src="https://sli.dev/logo-circle.png"
      alt=""
    />
    <img
      v-motion
      :initial="{ x: 600, y: 400, scale: 2, rotate: 100 }"
      :enter="final"
      class="absolute inset-0"
      src="https://sli.dev/logo-triangle.png"
      alt=""
    />
  </div>

  <div
    class="text-5xl absolute top-14 left-40 text-[#2B90B6] -z-1"
    v-motion
    :initial="{ x: -80, opacity: 0}"
    :enter="{ x: 0, opacity: 1, transition: { delay: 2000, duration: 1000 } }">
    Slidev
  </div>
</div>

<!-- vue script setup scripts can be directly used in markdown, and will only affects current page -->
<script setup lang="ts">
const final = {
  x: 0,
  y: 0,
  rotate: 0,
  scale: 1,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
</script>

<div
  v-motion
  :initial="{ x:35, y: 30, opacity: 0}"
  :enter="{ y: 0, opacity: 1, transition: { delay: 3500 } }">

[Slide Repo Link](https://github.com/benny123tw/github-action-introduction)

</div>

::right::

### References

* https://blog.gitea.com/creating-go-actions/
* https://blog.gitea.com/hacking-on-gitea-actions/
* https://docs.gitea.com/usage/actions/comparison
* https://docs.github.com/en/actions/sharing-automations/creating-actions/metadata-syntax-for-github-actions
* https://nektosact.com/not_supported.html
