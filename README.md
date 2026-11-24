# Git Collaboration Workshop

This repository contains a workshop to help people learn about how to collaborate using Git/GitHub. Supplementary slides can be found [here](https://docs.google.com/presentation/d/1wCAiCCtGlMs_8FMYvLU_UdESWoNnegtTNZBg-aP52O0/edit?usp=sharing)

## Setup and Merge Conflicts

### 1. Mirror the Repo 

To complete this workshop you will need to create a duplicate of this repo.
1. Create an empty repository on GitHub
2. Mirror this repo into your newly create one
```bash
git clone --mirror https://github.com/erlewa/git-collaboration-workshop 
cd git-collaboration-workshop.git
git push --mirror <your-repo-link>
```

Official documentation for this process is available [here](https://docs.github.com/en/repositories/creating-and-managing-repositories/duplicating-a-repository)

### 2. Merge the branches in order

Make Pull Requests for each branch _**in order**_ (`feat/merge-1`, `feat/merge-2`, etc) and try merging them into main! Some of them will have merge conflicts you have to resolve.

### 3. Setup your Development Environment
1. Create a virtual environment to isolate dependencies:
```bash
python3 -m venv .venv
source .venv/bin/activate
```

2. Install project dependencies
```bash
pip install --group dev
```

### 4. Test your program

Use `pytest` to make sure the final program is working before moving on to the rest of the workshop.
```bash
pytest
```

This should say that all checks passed (printed in green). If it says that any failed (this will be in red) something went wrong in the earlier steps. There is a correct version of the program available on the `post-merge-program` branch

## Group Collaboration
This segment is geared at giving you some hands on experience with collaboration in a GitHub repository. We encourage you to work through this section in a group of 2-3. If you can't find anyone to work with or you just don't like people then most of this section can be done solo but you might get less out of it than you would in a group setting. 

### 1. Share the Repo
One person per group should share their version of this repository with all other group members. GitHub has documentation for the process [here](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/repository-access-and-collaboration/inviting-collaborators-to-a-personal-repository)

Group members should recieve an invite in their email. Once they accept everyone should have write access to the repository.

### 2. Implementing New Features 
1. Each group member should select a feature from the list below to implement
 - Allow users to specify the character for the box
 - Allow users to specify a fill character 
 - Add a check to ensure user input is not negative

2. Each group member should create a new branch to work on
```bash
git switch -c <branch-name>
```
> Choose a naming convention to use for your branches! It is common to see something like `<initials>/<brief-description>`

3. Implement your feature
4. Create a Pull Request (PR) for your branch 
5. Get a group member to reviewa and approve your PR and then merge

