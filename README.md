# ArchGuard

Architecture

OpenSource processing

## Docker Organization
 - [archguard](https://hub.docker.com/orgs/archguard/repositories)

## 定位：架构治理
- 架构评估
- 架构改造
- 架构守护

目标用户：架构师
适用场景：向下管理，向上汇报，日常沟通

## 业务规划
### 核心域
- 架构评估
	- 代码反推架构
	- 架构坏味道
- 架构治理
	- 目标架构设计
	- 当前架构和目标架构对比
	- 通过配置/推荐的方法论，自动生成架构改进点，并配置/推荐架构演进路标
	- 配置/推荐团队当前组织架构，分配路标 owner
- 架构守护
	- 监控路标完成情况，按需更新目标架构
	- 路标完成做一次架构快照，追踪架构演进
	- 看板集成，追踪架构治理进度
### 支撑域
- 架构可视化
- 架构指标

## 开发规范更新：
- .github 定义贡献文档

## 重构策略：
- 把问题自动化重现出来
- 通过工具找出问题（自己重构自己）

## 电梯演讲
- 对于：架构师
- 他们想：提升向下管理，向上汇报，日常沟通的效率
- 这个：ArchGuard
- 是一个：架构治理工具
- 它可以：进行不同层级架构数据可视化，分析和评估
- 不同于：sonar
- 它的优势是：作为架构层面的工具集
