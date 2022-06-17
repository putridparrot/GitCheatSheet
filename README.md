# Git Cheat Sheet
A list of useful git CLI commands.

Git create a repository

| Command | Description |
|---------|-------------|
| git init _&lt;directory name&gt;_ | Initialize a repository locally |
| git clone _&lt;repository url&gt;_ | Clone a repository from a remote repo to your local machine |


Branches

| Command | Description |
|---------|-------------|
| git branch | List the branches within the repository |
| git branch --all | List the branches within the repository along with remotes |
| git branch --verbose | List the branches within the repository along with lastest commit |
| git branch -vv | List the branches within the repository along with lastest commit as well as origin |
| git checkout -b _&lt;branch-name&gt;_ | Create and checkout a branch with the branch-name |
| git branch branch-name | Create a branch but does not checkout |
| git branch -d _&lt;branch-name&gt;_ | Delete a branch which has been fully merge with upstream |
| git branch -D _&lt;branch-name&gt;_ | Force delete a branch whether merged or now |

Switching branches

| Command | Description |
|---------|-------------|
| git checkout _&lt;branch-name&gt;_ | Switch/checkout a branch using its branch-name |
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
| git rebase _&lt;branch&gt;_ | Rebases the current branch with the _branch_ |
| git rebase --continue | When rebasing, after any conflicts are resolved, run this command to contiue the rebase |


Logs

| Command | Description |
|---------|-------------|
| git log | List the log entries within the repository |
| git log  -_&lt;count&gt;_ | List the last _count_ log entries |


Git remote

_As git is a distributed source control system, we need ways to get changes from remote repos or push changes to them, whether
the remote repository is centralized, such as github or on another developers machine._

| Command | Description |
|---------|-------------|
| git push | Push changes to a remote repository |
| git pull | Pull changes from a remote repository |
| git fetch | Fetch changes from a remote repository without pulling them |
| git fetch -p | Fetch changes and prune/delete any remote deleted branches etc. |

Differences

| Command | Description |
|---------|-------------|
| git diff HEAD | Get the differences between your current code and last commit |
| git diff --cached | Get the differences between your current staged and last commit |
| git diff @{upstream} | Get the differences between your local branch and remote |

Cherry Picking

_Pick commits by their references and add to the current branch. This is a useful technique in situations
where a branch which you don't want to go live yet, had code that you need to pick out of that branch into
another one to go live with OR maybe you just committed changes to the wrong branch._

| Command | Description |
|---------|-------------|
| git cherry-pick _&lt;commit-ref&gt;_ | Cherry picks using the _commit-ref_ (the SHA) into the current branch HEAD |


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
