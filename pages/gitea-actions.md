---
layout: center
transition: fade-out
---

# Gitea vs GitHub Actions
https://docs.gitea.com/usage/actions/comparison

---
layout: center
---

- **Gitea Actions** allow actions written in pure Go
- **Git URL Flexibility:** Actions can run directly from arbitrary Git repositories (not limited to a marketplace)
- **Limited compatibility:** Some GitHub Actions features might not be fully supported in Gitea<sup>1</sup>

<Footnotes separator>
  <Footnote :number=1>Gitea's Actions are based on `nektos/act`, but with custom additions `gitea/act`. </Footnote>
</Footnotes>


<!--
2023/03/20
The nektos/act project is an excellent tool that allows you to run your GitHub Actions locally. We were inspired by this and wondered if it would be possible to run actions for Gitea.

However, while nektos/act is designed as a command line tool, what we actually need is a Go library with adjustments for Gitea. So we forked it as gitea/act.

This is a soft fork that will periodically follow the upstream. Although some custom commits have been added, we will try our best to avoid changing too much of the original code.
-->