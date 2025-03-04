# gha-practice
Github action practice repository for Language Technology conference 2022

## Setup
1. Create a branch named after your github user (or anything you like that noone else is likely to use)
2. Do not look at the grading.yml
3. Copy the template.yml file in the .github/workflows to a file with the same name you used for your branch
4. Commit and push your branch to the repo
5. Make a PR
6. Observe how the action interacts with your PR

## Next steps - Pick one of these and make it work
- Add a new step that runs dotnet build
- Run unit tests
- Add a new job
- Set an environment variable in one step and use it in another https://docs.github.com/en/actions/using-workflows/workflow-commands-for-github-actions#setting-an-environment-variable
- Set an output variable from one step and use it in another https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions#jobsjob_idoutputs
- Make your action get cancelled if you push while it is still running https://docs.github.com/en/actions/using-jobs/using-concurrency
- Add a matrix and use it (build platform is an obvious use) https://docs.github.com/en/actions/using-jobs/using-a-matrix-for-your-jobs
- Publish artifacts from your GHA build 
- Add conditions to a step https://docs.github.com/en/actions/using-jobs/using-conditions-to-control-job-execution
- Read the docs for basic understanding: https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions

## Existing lsdev Github Actions

https://github.com/sillsdev/docker-appbuilder-agent/blob/develop/.github/workflows/main.yml (builds docker image and pushes to AWS ECR and GHCR)
https://github.com/sillsdev/appbuilder-buildengine-api/blob/develop/.github/workflows/main.yml (builds docker image and pushes to GHCR)
https://github.com/sillsdev/appbuilder-portal/blob/develop/.github/workflows/main.yml (builds docker image, pushes to AWS ECR, and does blue/green deployment to ECS)
https://github.com/sillsdev/appbuilder-storybuilder/blob/main/.github/workflows/release.yml (on tag, creates release in GitHub which is downloaded via GitHub REST API during SAB build)
https://github.com/sillsdev/wesay/blob/develop/.github/workflows/PR.yml (matrix build and runs tests for Windows and Linux )
https://github.com/sillsdev/wesay/blob/develop/.github/workflows/Installer.yml (builds a Wix installer and uploads it as a Github artifact)
https://github.com/sillsdev/Mercurial4Chorus/blob/master/.github/workflows/nuget-ci-cd.yml (builds Nuget package and publishes to Nuget using Secrets)
