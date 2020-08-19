Want to undo committed changes?

If commited locally but haven't pushed upstream, then do this to unwind the commit and put the changes back in the STAGED area:
```
git reset --soft HEAD~1    # specify number of commits to unwind: 1,2,etc.
```

If you just want to get rid of the commit without bringing back the changes to STAGED, then do a hard reset:
```
git reset --hard HEAD~1    # WARNING WARNING WARNING
```

If committed locally and already pushed upstream, then don't change history because you don't know who may have pulled.
Perhaps use `git revert` to bring back previous version and push again.

But, if you're sure that nobody pulled from upstream, then you can unwind the commit and do `git push --force`.
