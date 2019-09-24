# Delete local branch 

```shell
git branch -d branch_name
git branch -D branch_name
git fetch --all --prune
```

**Note:** The `-d` option is an alias for `--delete`, which only deletes the branch if it has already been fully merged in its upstream branch. You could also use `-D`, which is an alias for `--delete --force`, which deletes the branch "irrespective of its merged status." 

# Delete Remote Branch [Updated on 8-Sep-2017]

```shell
git push <remote_name> --delete <branch_name>
git fetch --all --prune # used for propagating the changes
```

