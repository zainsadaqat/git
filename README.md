
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
