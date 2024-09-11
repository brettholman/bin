# This repository is a collection of shell scripts that will increase my productivity

Generally, for me, this will be stored in ~/.local/bin you will need to ensure that this repository is in your path.

## Dependencies

- bash/zsh/some shell
- tmux
- fzf

### wt-sync

This script is meant to handle untracked files while using git worktrees.
If you have files that you do not want to check into source control and have a repository that is utilizing worktrees you can follow the steps below:

```
git clone --bare $repository $repositoryDir
cd $repositoryDir
mkdir untracked
# Add files to the untracked dir that you want to be consistent between worktrees this can and should match the directory structure of $repository@main
# Navigate back to $repositoryDir (cd $repositoryDir)
wt-sync
# This will open up fzf with all of your active worktrees
# Search for the worktree you want to update, select it (tab and enter)
# And you should be all set
```

### tmux-sessionizer

This is blatantly taken from [theprimeagen](https://github.com/ThePrimeagen/.dotfiles/blob/master/bin/.local/scripts/tmux-sessionizer)
