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

## 初步计划
- 模型更新
  - 模型设计
    - 代码分析模型（当前Java）
    - 数据分析模型（Git等系统相关数据）
  - 模型替换
  - 模型持续维护
  
- 部署整合
  - flyway整合
  - deploy整合
  
- 前端服务划分
  - 分析现有前端服务
  - 整合/拆分前端服务
  
- 后端服务划分
  - 分析现有后端服务
  - 整合/拆分后端服务
  
- scanner
  - 分析现有scanner职责
  - 拆分/整合/替换现有scanner
  
- 前/后端代码规范
  - 分析现有代码规范
  - 制定代码规范
  - 添加代码规范保护



