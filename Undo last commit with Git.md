## Undoing the Last Commit with [[Git]]

However, of course, there a tons of situations where you _really_ want to undo that last commit. E.g. because you'd like to restructure it extensively - or even discard it altogether!

In these cases, the "reset" command is your best friend:

```sh
git reset --soft HEAD~1
```

Reset will rewind your current HEAD branch to the specified revision. In our example above, we'd like to return to the _one before the current_ revision - effectively making our last commit undone.

Note the --soft flag: this makes sure that the _changes_ in undone revisions are preserved. After running the command, you'll find the changes as uncommitted local modifications in your working copy.

If you don't want to keep these changes, simply use the --hard flag. Be sure to only do this when you're sure you don't need these changes anymore.

```sh
git reset --hard HEAD~1
```

[via](https://www.git-tower.com/learn/git/faq/undo-last-commit/)