# mirror-gitlab-github-ssh
Mirror repository from Gitlab to Github using Gitlab CI and ssh (Github deploy key)

Inspired by: https://gitlab.com/t-munk/gipsy

This project uses **ssh Github repository deploy key** instead of Github user access token.

**Repository deploy key** enables access to single repository.  
**User access token** enables access to all user repositories.  

## Setup
Add the following environment variables to the GitLab repository you want to push to GitHub:


`GITHUB_DEPLOY_KEY` (generate a new key using `ssh-keygen`)  
`GITHUB_REPO` (myuser/the-repo)


See .gitlab-ci.yml mirror task for an example, add this mirror stage your GitLab repository.

## Usage
Push a commit to eg. the master branch of your GitLab repository.
