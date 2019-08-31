# Amend Most Recent Commit Message

Make sure that you're in the right branch.

Update the commit message:
```
git commit --amend
```

If the commit has already been pushed before, you get an error while pushing.  For example:
```
$ git push
To https://github.com/tk3369/angular.git
 ! [rejected]            patch-1 -> patch-1 (non-fast-forward)
error: failed to push some refs to 'https://github.com/tk3369/angular.git'
hint: Updates were rejected because the tip of your current branch is behind
```

In that case, you can force push.
```
git push --force
```
