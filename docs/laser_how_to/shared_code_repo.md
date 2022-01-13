---
layout: default
title: Shared Code Repositories
parent: LASER How To
nav_order: 8
---

## Shared code between LASER VREs

Subject to sufficient justification and security controls, it is possible to enable code collaboration between VREs via a shared remote repository. If you are interested in enabling this functionality, the PIs of both VREs should contact the (Data Analytics Team)[mailto:dat@leeds.ac.uk] to explain the use case.

If the request for code collaboration has been granted, the below guide describes how you can create a remote repository and share it between VREs.

### Create remote repository on the code share

- Make sure Git has been installed to your virtual machine via Software Centre. Open Git Bash.
- A shared storage area will be mapped to X: drive in both VREs. Type `/x/` in Git Bash to navigate to this drive.
- Create the folder for your remote repository on X: drive by typing `mkdir demo_repo`, replacing demo_repo with your chosen folder name at this step and steps thereafter.
- Navigate into the folder: `cd demo_repo`
- Initialise the folder as a git repository: `git init`
- Commit your first code, such as a README, to your repository. You have created a repository that is accessible to both VREs.

## Create local repository in each VRE

- Open Git Bash and navigate to where you want to put the code repository in your VRE's shared storage on N: drive: `cd /n/path/to/local/repo/`
- Clone the remote repository on X: drive to create a local copy: `git clone -l /x/demo_repo`
- You should now have a local clone of your code repository at `/n/path/to/local/repo/demo_repo`
- You can push and pull between the local and remote repository as you would usually do. When set up from both VREs, this will enable code collaboration via the remote repository.
