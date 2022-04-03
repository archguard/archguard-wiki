## 版本管理

基于：[git-filter-repo](https://htmlpreview.github.io/?https://github.com/newren/git-filter-repo/blob/docs/html/git-filter-repo.html) 的代码过滤

项目中包含了密钥等内容，需要从 Git 历史中消除，以确保安全。

文档：[Splitting a subfolder out into a new repository](https://docs.github.com/en/get-started/using-git/splitting-a-subfolder-out-into-a-new-repository)

1. 安装 [filter-repo](https://github.com/newren/git-filter-repo/blob/main/INSTALL.md)


### git 操作：只保留某目录

```
$ git filter-repo --path FOLDER-NAME1/ --path FOLDER-NAME2/
# Filter the specified branch in your directory and remove empty commits
> Rewrite 48dc599c80e20527ed902928085e7861e6b3cbe6 (89/89)
> Ref 'refs/heads/BRANCH-NAME' was rewritten
```

### git 操作：反向删除某个目录 

```
$ git filter-repo --path FOLDER-NAME1/ --path FOLDER-NAME2/  --invert-paths 
# Filter the specified branch in your directory and remove empty commits
> Rewrite 48dc599c80e20527ed902928085e7861e6b3cbe6 (89/89)
> Ref 'refs/heads/BRANCH-NAME' was rewritten
```

### git 操作：合并代码库，保持 commits 历史

[How do you merge two Git repositories?](https://stackoverflow.com/questions/1425892/how-do-you-merge-two-git-repositories)

```
cd path/to/project-b
git remote add project-a /path/to/project-a
git fetch project-a --tags
git merge --allow-unrelated-histories project-a/master # or whichever branch you want to merge
git remote remove project-a
```
