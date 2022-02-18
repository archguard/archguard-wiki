# ArchGuard

Architecture

OpenSource processing

## Frontend

- [x] [ArchGuard CLI](https://github.com/archguard/arch-guard-cli)
- [ ] ArchGuard Frontend
- [x] ArchGuard.org 开源

## Backend

- [ ] architecture fitness model (new)
- [ ] Scanner
   - [ ] dependencies_java
   - [ ] scan_java_bytecode
   - [ ] scan_git  
   - [ ] scan_jacoco 
- [ ] Backend services

# Opensource notes

## 版本管理

基于：[git-filter-repo](https://htmlpreview.github.io/?https://github.com/newren/git-filter-repo/blob/docs/html/git-filter-repo.html) 的代码过滤

项目中包含了密钥等内容，需要从 Git 历史中消除，以确保安全。

文档：[Splitting a subfolder out into a new repository](https://docs.github.com/en/get-started/using-git/splitting-a-subfolder-out-into-a-new-repository)

1. 安装 [filter-repo](https://github.com/newren/git-filter-repo/blob/main/INSTALL.md)
2. 
### Git 操作：只保留某目录

```
$ git filter-repo --path FOLDER-NAME1/ --path FOLDER-NAME2/
# Filter the specified branch in your directory and remove empty commits
> Rewrite 48dc599c80e20527ed902928085e7861e6b3cbe6 (89/89)
> Ref 'refs/heads/BRANCH-NAME' was rewritten
```

### GIt 操作：反向删除某个目录 

```
$ git filter-repo --path FOLDER-NAME1/ --path FOLDER-NAME2/  --invert-paths 
# Filter the specified branch in your directory and remove empty commits
> Rewrite 48dc599c80e20527ed902928085e7861e6b3cbe6 (89/89)
> Ref 'refs/heads/BRANCH-NAME' was rewritten
```


## 定位

架构分析可视化

待讨论：
- 是平台，还是工具？
- 和其他工具集的关系？

## 基础需求
- 数据可视化
- 灵活配置
- 支持多语言，多框架

## 路线图
- 模型更新
  - 模型设计
    - 代码分析模型（当前Java）
    - 数据分析模型（Git等系统相关数据）
  - 模型替换
  - 模型维护策略
  
- 部署整合
  - flyway整合
  - deploy整合

- 基础设施迁移
  - maven to gradle
  
- 前端服务划分
  - 分析现有前端服务
  - 整合/拆分前端服务
  
- 后端服务划分
  - 分析现有后端服务
  - 整合/拆分后端服务
  
- scanner
  - 分析现有scanner职责
  - 拆分/整合/替换现有scanner
  
- 文档更新
  - 现有文档更新
  - 文档维护策略制定
  
- 前/后端代码规范
  - 代码规范制定
  - 代码规范保护策略
  
- 线上环境
  - 是否保留线上环境（决策）
  - 各环境维护
  - 流水线搭建
  
- 官网维护
  - 官网内容定时更新
  - 官网博客


