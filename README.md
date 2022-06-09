# Git CheatSheet
A list of useful git CLI commands.

Git create a repository

| Command | Description |
|---------|-------------|
| git init | Initialize a repository locally |
| git clone https://github.com/putridparrot/GitCheatSheet.git | Clone a repository from a remote repo |


Git branches/tags

| Command | Description |
|---------|-------------|
| git branch | List the branches within the repository |
| git tags | List the tags within the repository |
| git checkout -b branch-name | Create and checkout a branch with the branch-name |
| git branch branch-name | Create a branch but does not checkout |

Git remote

| Command | Description |
|---------|-------------|
| git push | Push changes to a remote repository |
| git pull | Pull changes from a remote repository |
| git pull | Pull changes from a remote repository |

Git repository status

| Command | Description |
|---------|-------------|
| git status | Displays information about the current repo status |


Git basic commands

| Command | Description |
|---------|-------------|
| git --version | Displays the current git version |

Other useful commands

| Command | Description |
|---------|-------------|
| git branch &#124; grep search-pattern &#124; xargs git checkout | Supply a search pattern (such as an issue id) and if a single branch exists, check it out |