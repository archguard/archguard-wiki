# ArchGuard

Architecture

OpenSource processing

## Frontend

- [ ] [ArchGuard CLI](https://github.com/archguard/arch-guard-cli)
   - [ ] code check
   - [ ] license check
   - [ ] history check
   - [ ] secret key check
   - [ ] setup document check
- [ ] ArchGuard Frontend
   - [ ] code check
   - [ ] license check
   - [ ] history check
   - [ ] secret key check
   - [ ] setup document check

## Backend

- [ ] architecture fitness model (new)
   - [ ] document check
- [ ] Scanner
   - [ ] dependencies_java
   - [ ] scan_java_bytecode
   - [ ] scan_git  
   - [ ] scan_jacoco 
- [ ] Backend services
   - [ ] code check
   - [ ] license check
   - [ ] history check
   - [ ] secret key check
   - [ ] setup document check


# Opensource notes

## 版本管理

### Git 操作：只保留某目录

项目中包含了密钥等内容，需要从 Git 历史中消除，以确保安全。

文档：[Splitting a subfolder out into a new repository](https://docs.github.com/en/get-started/using-git/splitting-a-subfolder-out-into-a-new-repository)

1. 安装 [filter-repo](https://github.com/newren/git-filter-repo/blob/main/INSTALL.md)

```
$ git filter-repo --path FOLDER-NAME1/ --path FOLDER-NAME2/
# Filter the specified branch in your directory and remove empty commits
> Rewrite 48dc599c80e20527ed902928085e7861e6b3cbe6 (89/89)
> Ref 'refs/heads/BRANCH-NAME' was rewritten```
```




