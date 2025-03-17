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
  <Footnote :number=1>Gitea's Actions are based on Act, but with custom additions `gitea/act`. </Footnote>
</Footnotes>
