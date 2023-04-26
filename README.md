# Auto Merge Dependabot Pull Requests

I am assuming `main` branch is a protection branch, and setting branch protection rules.

## Branch protection rule
1. In your repository navigation to Settings > Branches
1. Under “Branch protection rules” select `Add branch protection rule`
1. Branch name pattern -> main
1. Enable the following settings
    1. Require a pull request before merging
    1. Require approvals
    1. Require status checks to pass before merging -> Prevent merging pull requests with failing build
    1. Require branches to be up to date before merging

See the following picture:
![alt text](pictures/actions-automerge-dependabot-prs01.png)

## GITHUB_TOKEN permissions
1. In your repository navigation to Settings > Actions > General
1. Under “Workflow permissions” enable the following settings
    1. Read and write permissions
    1. Allow Github Actions to create and approve pull requests

See the following picture:
![alt text](pictures/actions-automerge-dependabot-prs02.png)

## Store credentials for Dependabot to use
To give Dependabot access to the private registries supported by GitHub, you store the registry’s access token or secret in the secret store for your repository or organization.

+ In your repository navigation to Settings > Secrets and variables > **Dependabot** > New repository secret
