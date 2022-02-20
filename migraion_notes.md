# Backend

 - 合并了 code-analysis
 - 合并了 code-addition
 - 合并了 flyway-services
 - 合并了 code-scanner
 - 干掉了 eureka
 - 自动发布到 GitHub release by tags
 - GET hub/sizing/cohesion/redundancy 等的请求，构建为统一的 POST 以及 `FilterSizingDto`

遗留问题：

 - code-scanner 有一些依赖于数据库的 test 有问题

# Frontend

 - 删除了遗留的版权问题代码 by history
 - 没有用户体系，所以修改了默认用户
 - 从历史线上抹除了 `test/` 相关的页面

# Scanner

 - 从历史线上，只保持了 jacoco, git
 - 使用 fatjar 构建 jar 包，发布到了 GitHub release

