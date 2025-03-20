## Resources

* https://blog.gitea.com/creating-go-actions/
* https://blog.gitea.com/hacking-on-gitea-actions/
* https://docs.gitea.com/usage/actions/comparison
* https://docs.github.com/en/actions/sharing-automations/creating-actions/metadata-syntax-for-github-actions
* https://nektosact.com/not_supported.html

## Differences

* Gitea Actions are written in Go.
* Gitea Actions are executed in a Docker container.
* Gitea Actions can run actions in pure Go code.
* Gitea Actions supports actions from arbitrary Git URLs

This is why we can't run `act` tool to test Gitea Actions, unless we don't use those additional features.

## How to run Gitea Actions locally?
