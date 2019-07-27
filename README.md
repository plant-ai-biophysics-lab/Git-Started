# Git started

<h4><b> A walkthrough of the Plant AI and Biophysics Lab's git workflow. </b></h4>

## Terminology

Here are some of my loose definitions of basic git concepts...

<i>Agents</i>
- <b>Version control system</b>: A system that records changes to a file or set of files over time so that you can recall specific versions later.
- <b>GitHub repository</b>: Often shortened to 'repo', a version controlled codebase.
- <b>GitHub organization</b>: A collection of team members and external collaborators that are working together to build one or more repos.
- <b>Member</b>: A person belonging to a GitHub organization.
- <b>Collaborator</b>: A person contributing to a given repo.

<i>Objects</i>
- <b>Codebase</b>: All of the code (and non-code) files that constitute your software.
- <b>Local</b>: The computer that you're currently working on.
- <b>Remote</b>: The computers maintained by GitHub in some server farm where you store all your repos.
- <b>Branch</b>: One of many possible active versions of a codebase, either local or remote.

<i>Actions</i>
- <b>Clone</b>: To copy a repository from the remote server to a local machine for the first time.
- <b>Pull</b>: To update a local branch based on the latest version on the remote server.
- <b>Status</b>: Tells you which files in your current branch are different from the remote server.
- <b>Add</b>: Stage files from your current branch for upload to the version on the remote server.
- <b>Commit</b>: Instate local changes and prepare for upload to remote server.
- <b>Push</b>: Upload changed and committed files to the remote server.
- <b>Checkout</b>: Switch to a different (either new, locally hosted, or remotely hosted) branch
- <b>Merge</b>: Combine two branches together. <b>This can be a little tricky!</b>


## Our basic workflow

We use a `master` <-> `dev` <-> `dev_<insert-name>` development workflow. Two branches, `master` and `dev`, require a pull request (PR) prior to merging new code. Contributors to a repo can create any additional number of `dev_<insert-name>` branches. These third-order branches are where new software features are born. We try to keep a 1:1 feature to branch mapping. That means each branch should be associated with *a single* feature. Prior to merging into the `dev` branch, and once you've tested your `dev_<insert-name>` code sufficiently, you can ask one or more collaborators to review it by making a PR. Following several merges of different `dev_<insert-name>` branches into `dev` it's probably worthwhile to merge `dev` into `master`. This event should be accompanied by releasing a new version, e.g. `v0.1`.

As an example, let's say that I want to develop a new software feature. I'll do the following:

1. Clone the repo, which starts as the `master` branch.
2. Checkout the existing `dev` branch from the remote.
3. Checkout a new `dev_<insert-name>` branch on your local machine.
4. CODE TEST CODE TEST CODE TEST CODE TEST .... CODE TEST ... =)
5. Submit a PR to a collaborator. 
6. Wait for PR approval or suggestions for edits.
7. Once PR approved, merge into `dev` branch on local.
8. Add, commit and push updated version of `dev` to remote. 
9. Delete local and remote copies of `dev_<insert-name>` branch.
10. Start again.

### Cloning a repo

The first thing you'll want to be able to do is <b>clone</b> a Github repository. 

```bash
$ git clone https://github.com/<organization>/<repository-name>.git
```

You can grab the repo URL from the remote repo. For example,

![test image](images/clone_with_https_screenshot.png)

### Checking out a new branch

## Advanced workflow

Coming soon!
