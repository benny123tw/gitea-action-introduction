# Agenda

## The goal of this talk

- Learn what Gitea Actions are
- Hope to inspire you to convert your GitHub Actions to Gitea Actions

## A brief history of Gitea runners compared to GitHub runners

- Gitea uses `act` to run GitHub Actions locally
- Gitea forked `act` and made some changes to it - `gitea/act`

## The difference between Gitea Actions and GitHub Actions

- You can write actions in pure Go
- You can run actions from arbitrary Git URLs

## How to write a Gitea/GitHub Action

- Start with `action.yml` file
  - Define inputs and outputs
  - Define how to run the action
- Write the action code
  - In Go (Gitea specific)
  - In any language that can be containerized
- Test the action locally
  - Using `act` for GitHub Actions
  - Using `gitea/act` for Gitea Actions
- Publish the action
  - To GitHub/Gitea repository
  - Make it available for others

## Demo with a TypeScript action

- Create a new project
- Write the action code
- Test and debug
- Package and release

## How to run a Gitea Action

- introduce workflow file
- run workflow
- debug workflow
- run workflow with inputs and outputs
- run workflow with secrets
- run workflow with artifacts

## How to convert a GitHub Action to a Gitea Action

- Convert the action code
- Convert the workflow file
- Test the action locally
- Publish the action