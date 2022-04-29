# Reset to a previous commit

Lets say you have a couple of commits within your current branch, but you want to go back to a previous commit within this branch and discard everything after that commit. This page will tell you how to do this.

## Comment line solution

First of all you need to be inside a branch thats not the master branch. And you need to have done more than one commit in your current branch. 

Run `git reset --hard [commit]`, use the id(can be found on github) of the desired commit you want to reset to as commit value. This will set you local HEAD to that of the chosen commit. 

Now when you do your next commit, you do so just as you would with one exception. When pushing the commit use the `--force` flag. This will delete the commits done after the current branch before resetting. 

!> **Caution!** This can't be reversed! Your commits after the commit you reset will be lost!

#### To summarize:
- Run: `git reset --hard [commit]`
- Make you changes
- Add: `git add .`
- Commit: `git commit -m "commit description"`
- Push: `git push --force`

