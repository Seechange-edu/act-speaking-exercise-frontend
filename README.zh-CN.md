# AI English Gym 工作流执行器

[English](README.md)

私有前端以 `changelog-summary` 事件发送按 UTC+8 包含首尾两天的日期范围，以及可选
`backend,aiTutor,website,cms` 来源键。内容始终只包含 AI English Gym／Think & Speak，
即使选择 CMS，其余模块也自动排除，不提供内容范围开关。共用执行器保留单版本默认行为，
复用 ACTION_TOKEN、AWS 和 SSM 配置。保持 `quiet`，报告只附加到私有前端 Release。
启用前先发布 api-meter 汇总迁移及 repo-toolkit main。

普通单版本 `joint` changelog 也使用相同模块边界：填写的 `cms` tag 会贡献其 Think & Speak
页面的改动，包括学生端未改变的教师/管理员页面更新。其他 CMS 模块即使提到 Think & Speak
也不会纳入。启用 CMS diff 读取前，先部署 api-meter 路由迁移 `e2513a0d7f26`。
