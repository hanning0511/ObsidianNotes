# Git

## 删除本地和远程 tag

### 删除本地 tag

```shell
$ git push --delete <remote> <tag name>
```

### 删除远程 tag

```shell
$ git tag -d <tag name>
```

### 从仓库中永久删除某个文件

```shell
$ git filter-branch --force --index-filter \
  'git rm --cached --ignore-unmatch <path/to/file>' \
  --prune-empty --tag-name-filter cat -- --all
```