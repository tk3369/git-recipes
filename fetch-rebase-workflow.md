Suppose that you're working on a branch but the main branch at the remote `origin` has moved on. 

To get up to speed to the latest changes while you're on your own branch:

```
git fetch origin main:main        # or master branch 
git rebase main
```

The second command could be done more clearly as:
```
git rebase main YOURBRANCH
```

Now, if `YOURBRANCH` has been pushed to GitHub before, then you cannot push again after rebase unless you use the force option:

```
git push -f
```

After that, if you try to pull from GitHub from another location, you may see a message that looks like:

```
On branch X
Your branch and 'origin/X' have diverged,
and have N and M different commits each, respectively.
  (use "git pull" to merge the remote branch into yours.)
```

But then, do not just use `git pull` because it would create a merge commit, whic isn't what we want for the rebase workflow. Instead, do this:

```
git pull --rebase
```

And it should work and give you a nice message:
```
First, rewinding head to replay your work on top of it...
```
