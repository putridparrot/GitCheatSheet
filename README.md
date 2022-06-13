# Git Cheat Sheet
A list of useful git CLI commands.

Git create a repository

| Command | Description |
|---------|-------------|
| git init {directory name} | Initialize a repository locally |
| git clone {repository url} | Clone a repository from a remote repo to your local machine |


Branches

| Command | Description |
|---------|-------------|
| git branch | List the branches within the repository |
| git branch --all | List the branches within the repository along with remotes |
| git branch --verbose | List the branches within the repository along with lastest commit |
| git branch -vv | List the branches within the repository along with lastest commit as well as origin |
| git checkout -b branch-name | Create and checkout a branch with the branch-name |
| git branch branch-name | Create a branch but does not checkout |
| git branch -d branch-name | Delete a branch which has been fully merge with upstream |
| git branch -D branch-name | Force delete a branch whether merged or now |

Switching branches

| Command | Description |
|---------|-------------|
| git checkout branch-name | Switch/checkout a branch using its branch-name |
| git checkout - | Switch/checkout the previous checked out branch |

Tags

_Tags are usually used to store the state of code a specific point. The most obvious use is when we release new versions of our code we tag the release so we have a tag with the name v1.0.1 (for example). Meaning if we need to review the released code
we can simply checkout our tags._

| Command | Description |
|---------|-------------|
| git tag | List the tags within the repository |
| git fetch --all --tags | Fetch all tags from a remote repository |
| git tag -d v1.0.1 | Delete a tag named v1.0.1 |

Stash

_Stash allows us to store changes temporarily within "stash". For example we're midway through changes in our code and need to stash the changes whilst we revert switch branches, then when we switch back we can pop from the stash to get back our code without the need to commit partially completed work._

| Command | Description |
|---------|-------------|
| git tag | List the tags within the repository |

Rebase

_Rebasing your branch basically rolls back your changes, applies the rebase changes then adds your changes back. This
is often used in place of merging if, for example, the branch you have branched from has additional changes to it and you
want to or need to bring those changes into your branch._

| Command | Description |
|---------|-------------|
| git rebase {branch} | Rebases the current branch with the {branch} |
| git rebase --continue | When rebasing, after any conflicts are resolved, run this command to contiue the rebase |


Logs

| Command | Description |
|---------|-------------|
| git log | List the log entries within the repository |
| git log  -{count} | List the last {count} log entries |


Git remote

_As git is a distributed source control system, we need ways to get changes from remote repos or push changes to them, whether
the remote repository is centralized, such as github or on another developers machine._

| Command | Description |
|---------|-------------|
| git push | Push changes to a remote repository |
| git pull | Pull changes from a remote repository |
| git fetch | Fetch changes from a remote repository without pulling them |
| git fetch -p | Fetch changes and prune/delete any remote deleted branchs etc. |

Status

| Command | Description |
|---------|-------------|
| git status | Displays information about the current repo status |


Basic Commands

| Command | Description |
|---------|-------------|
| git --version | Displays the current git version |

Other useful commands/combinations of commands

| Command | Description |
|---------|-------------|
| git branch &#124; grep search-pattern &#124; xargs git checkout | Supply a search pattern (such as an issue id) and if a single branch exists, check it out |
