---
title: Useful Git commands
tags: Development Git HowTo
permalink: /dev/useful-git/
---

## How To

### Copy a git repo without history

```bash
git --depth <depth>
# Create a shallow clone with a history truncated
# to the specified number of revisions.
```

- [git documentation](https://git-scm.com/docs/git-clone)

### Stash the changes in a dirty working directory away

```bash
git stash
git status
git log
...
git stash pop
git status
```

### Update submodules

```bash
git submodule update --init --recursive
# download up to 8 submodules at once
git submodule update --init --recursive --jobs 8
git clone --recursive --jobs 8 [URL to Git repo]
# short version
git submodule update --init --recursive -j 8
# pull all changes in the repo including changes in the submodules
git pull --recurse-submodules
# pull all changes for the submodules
git submodule update --remote
### etc
```

- [Update submodules](https://www.vogella.com/tutorials/GitSubmodules/article.html)

### Rebase from the last "good" commit

identify the last "good" commit and provide its hash to the rebase command:

```batch
git rebase -i -p 0ad14fa5
```

### How to combine two commits into one commit?

```bash
git rebase -i
```

It performs an interactive rebase.
If you’re currently on your “commit 1”, and the commit you want to merge, “commit 2”, is the previous commit, you can run

```bash
git rebase -i HEAD~2
```

and change the first word of the second line from “pick” to “squash”. Then write your file, and quit. Git will squash your first commit into your second last commit.

### How to add a file to the last commit in git?

```bash
git add .
git commit --amend --no-edit
```

### How to squash commits in git after they have been pushed?

Squash commits locally with

```bash
git rebase -i origin/featurebranch~4 featurebranch
```

and then force push with

```bash
git push origin +featurebranch
```

featurebranch – can be master also

### How can I undo the last commit?

```bash
git reset --soft HEAD~1
```

Reset will rewind your current HEAD branch to the specified revision. In our example above, we’d like to return to the one before the current revision – effectively making our last commit undone.

Note the –soft flag: this makes sure that the changes in undone revisions are preserved. After running the command, you’ll find the changes as uncommitted local modifications in your working copy.

If you don’t want to keep these changes, simply use the –hard flag. Be sure to only do this when you’re sure you don’t need these changes anymore.

```bash
git reset --hard HEAD~1
```

or

```bash
git reset --hard origin/master
```

- [How can I undo the last commit?](https://www.git-tower.com/learn/git/faq/undo-last-commit)

### How change the author name / email of a commit?

- Changing the Author Information Just for the Next Commit  
  Finally, with the --author flag, you can also overwrite the author information for just the next commit:  

  ```batch
  git commit --author="John Doe <john@doe.org>"
  ```

- Using --amend for the Very Last Commit  
  In case you want to change just the very last commit, Git offers a very easy way to do this:  

  ```batch
  git commit --amend --author="John Doe <john@doe.org>"
  ```

  This effectively replaces the last commit with your "edited" version, correcting the wrong author information.

- Using Interactive Rebase  
  The first step is to identify the last "good" commit and provide its hash to the rebase command:

  ```batch
  git rebase -i -p 0ad14fa5
  ```  

  Your editor will open, requesting you to mark all the commits you want to change with the "edit" keyword.  
  Your job, now, is to **correct the author information** and then **continue to the next concerned commit** object until you've edited all the commits you just marked:  

  ```batch
  git commit --amend --author="John Doe <john@doe.org>" --no-edit
  git rebase --continue
  ```

- [source](https://www.git-tower.com/learn/git/faq/change-author-name-email/)

### Remove Untracked Files

Before running the actual command and removing untracked files and directories use the -n option that will perform a “dry run” and show you what files and directories will be deleted:

```bash
git clean -d -n {dir_path}
```

If some of the files listed above are important, you should either start tracking these files with git add <file> or add them to your .gitignore.

Once you are sure you want to go ahead and delete the untracked files and directories, type (beware: this will delete files):

```bash
git clean -d -f {dir_path}
```

- [Remove Untracked Files](https://linuxize.com/post/how-to-remove-untracked-files-in-git/)
- [How to remove local untracked files from the current git working tree](https://stackoverflow.com/questions/61212/how-to-remove-local-untracked-files-from-the-current-git-working-tree/18974433#18974433)
- [How to remove local untracked files from the current Git branch](https://koukia.ca/how-to-remove-local-untracked-files-from-the-current-git-branch-571c6ce9b6b1)

### How merge two commits

```bash
git rebase -i HEAD~2
```

or

```bash
git rebase --interactive HEAD~2
```

### How to permanently remove few commits from remote branch

```bash
git reset --hard HEAD~1
```

your local branch to remove changes from working tree and index.

and

```bash
git push --force origin feature
```

your revised local branch to the remote.

### Fixing conflict between master and feature branch

Fixing via rebase:

```bash
git checkout master
git pull                 # gets latest changes made to master
git checkout feature     # switch to your feature branch
git rebase master        # rebase your branch on master
# complete the rebase, fix merge conflicts, etc.
git push --force origin feature
```

Note carefully that the –force option on the push after rebasing is probably required as the rebase effectively rewrites the feature branch. This means that you need to overwrite your old branch in GitHub by force pushing.

Regardless of whether you do a merge or a rebase, afterwards the conflicts should be resolved and your reviewer should be able to complete the pull request.

or:

```bash
git fetch -p
git rebase origin/master
git push --force-with-lease
```

Fixing via merge:

```bash
git fetch origin         # gets latest changes made to master
git checkout feature     # switch to your feature branch
git merge master         # merge with master
# resolve any merge conflicts here
git push origin feature  # push branch and update the pull request
```

- [stackoverflow](https://stackoverflow.com/a/40864334)

### How to keep a git branch in sync with master

```bash
git remote update
git rebase origin/master
```

or

```bash
git checkout master
git pull
git checkout thefuturebranch
git merge master
```

### Reset the local master to the origin master (or Git force pull to overwrite local files)

```bash
git fetch origin master
git reset --hard origin/master
git clean -f -d
```

or

```bash
git fetch --all
git reset --hard origin/master
git pull origin master
```

Warning: this is a hard reset, it will lose all your changes (committed* or not).

### Viewing unpushed Git commits

```bash
git log origin/master..HEAD
```

or

```bash
git log --stat origin/master..HEAD
```

You can also view the diff using the same syntax

```bash
git diff origin/master..HEAD
```

If you want to see all commits on all branches that aren’t pushed yet, you might be looking for something like this:

```bash
git log --branches --not --remotes
```

And if you only want to see the most recent commit on each branch, and the branch names, this:

```bash
git log --branches --not --remotes --simplify-by-decoration --decorate --oneline
```

### Renaming Git Branch

```bash
git branch -m {new_name}
```

### Create Git Patch for Specific Commit

```bash
git format-patch -1 {commit_sha}
```

- [Creating and Applying Git Patch Files](https://nithinbekal.com/posts/git-patch/)

### Apply Git Patch Files

```bash
git apply {patch_file}
```

### An internal housekeeping utility that deletes lost or "orphaned" Git objects

```bash
git prune
```

### Solution removing the history

to prune the old commits. This makes the old commits and their objects unreachable:

```bash
git fetch --depth=1
```

To expire all old commits and their objects:

```bash
git reflog expire --expire-unreachable=now --all
```

to remove the old objects:

```bash
git gc --aggressive --prune=all
```

- [stackoverflow](https://stackoverflow.com/a/37099824)

