Suppose that you're working on a branch but the main branch has moved on. To get up to speed to the latest changes:

```
git fetch origin main:main          # or master branch
git rebase main YOUR_BRANCH
```
