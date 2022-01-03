
# How to Undo Mistakes in Git using Command Line

### 1. Discarding all local changes in a file

You make some changes in a local file and haven't make a commit yet and noticed it's not a better version and you want to go to the last commited version.

`git restore <file_name>`

> Note: Discarding uncommitted local changes can not be undone!

### 2. Restoring deleted files

You not only make some changes but also deleted that file and you want that file back

`git restore <file_name>`

### 3. Discard chunks

We want to keep the first and get rid of second part of the changes.

`git restore -p <file_name>`

### 4. Discarding all local changes

Remove everything we did just before the last commit

`git restore .`

Note: Please be careful with this command. Discarding uncommitted local changes can not be undone!

### 5. Fixing the last commit

`git commit --amend -m "Commit message`

> Note: --amend rewrites history! never change history for commits that have already been pushed to a remote repository!

### 6. Reverting a commit in the middle

`git revert <commit_hash>`

git revert creates a new commit that revert the effect of specified commit

### 7. Resetting to an old revision

`git reset --hard <commit_hash>`

git reset sets your HEAD pointer to an older revision. Commits after this revision appears to be undone!

### 8. Resetting a file to an older revision

`git restore --source <commit_hash> <file_name>`

### 9. Reflog - Recovering deleted commits

if you reset your HEAD to an old revision and all the commits after that revision will be gone. So if you think that was an accident you can get that back.

`git reflog`

`git branch branch_name <commit_hash>`

### 10. Reflog - Recovering deleted branch

`git reflog`

`git branch branch_name <commit_hash>`

### 11. Moving commit to a new branch

when You committed on main or develop branch directly. Move to the new branch first and move HEAD 1 commit behind.

`git branch feature/branch_name`

`gir reset HEAD~1 --hard`

### 12. Moving commit to a different branch

In this case feature branch is already present.

`git checkout feature_branch`

`git cherry-pick <SHA>`

`git checkout main`

`git reset --hard HEAD~1`

## Interactive Rebase

### 13. Edit old commit message

First check how many commits you want to go back. if it was the last commit then you can amend it easily by amend command. if not then:

`git rebase -i HEAD~COMMIT_NUMBER`

An editor window will be opened. Commits will be shown in reverse order means last one will be the lastest commit.

replace `pick` with `reword` and edit the commit message and then save the file.

### 14. Deleting old commit message

`git rebase -i HEAD~COMMIT_NUMBER`

replace `pick` word with `drop`

## Author

👤 **Zain Sadaqat**

- GitHub: [@zainsadaqat](https://github.com/zainsadaqat)
- Twitter: [@zain_sadaqat](https://twitter.com/zain_sadaqat)
- LinkedIn: [zain-sadaqat](https://linkedin.com/in/zain-sadaqat)

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

Feel free to check the [issues page](../../issues/).

## Show your support

Give a ⭐️ if you like this project!

## Acknowledgments

- Git Tower
- FreeCodeCamp

## 📝 License

This project is [MIT](./MIT.md) licensed.
