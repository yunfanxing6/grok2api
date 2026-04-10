# Grok2API Fork 说明

这是基于上游 `chenyme/grok2api` 的自用修复分支说明。

当前兼容发布基线：`1.6.2-grok.1`

当前这份 fork 主要补了以下几类问题：

## 已做修复

- 图片模型别名兼容：
  - `grok-imagine-1.0-fast`
- 图片/视频 429 错误更明确地透传
- 媒体 token 池优先级优化
- 图片编辑链路修复：
  - `grok-imagine-1.0-edit`
- 图片/视频生成结果解析修复
- function imagine / video SSE 错误码透传更一致
- 继续保持和 `sub2api-grok` 的现有对接协议兼容

## 目的

让它更适合作为 `sub2api-grok` 的 Grok 上游。

也就是说：

- `sub2api` 负责用户、API Key、计费、后台
- 这个 `grok2api` fork 负责真正访问 Grok 上游

## 当前联调状态

已验证：

- 文本
- 文生图
- 图生图/编辑
- 文生视频

如果你准备公开部署，建议和 `sub2api-grok` 一起使用。

## 关于上游更新

上游 `chenyme/grok2api` 后续已经进入 `v2.x` 重构阶段，但这份 fork 当前仍以兼容现有 `sub2api-grok` 接入为优先目标。

因此这次发布采用的是：

- 保留现有 `v1.x` 兼容接口行为
- 吸收适合当前架构的上游基线更新
- 不直接切换到 `v2.x` 的大重构目录结构
