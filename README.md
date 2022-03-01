# ArchGuard

Architecture

OpenSource processing

## Docker Organization
 - [archguard](https://hub.docker.com/orgs/archguard/repositories)

# Opensource notes

## 定位：架构治理
- 架构评估
- 架构改造
- 架构守护

目标用户：架构师
适用场景：向下管理，向上汇报，日常沟通

目标
- 展示架构现状，以及理想状态和现实状态的差距，提供给架构师分析
- ArchGuard 作为 Pipline ，插件化各流程，基于模型来分析评估
	- 扫描（定制）-》基于模型进行分析（标准化）-》评估（配置）
- 聚焦更有价值的功能
	- 架构数据可视化 （已有功能，待改进）
	- 服务内依赖关系分析 （已有功能，待改进）
	- 微服务依赖关系分析（新功能适配，分布式单体问题）
	- 架构配置，默认推荐 or 自定义

当前目标：做出一个模型汇报（如C4）MVP

开发规范更新：
- .github 定义贡献文档

重构策略：
- 把问题自动化重现出来
- 通过工具找出问题（自己重构自己）

电梯演讲
- 对于：架构师
- 他们想：提升向下管理，向上汇报，日常沟通的效率
- 这个：ArchGuard
- 是一个：架构治理工具
- 它可以：进行不同层级架构数据可视化，分析和评估
- 不同于：sonar
- 它的优势是：作为架构层面的工具集


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


