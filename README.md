# System Design

## 1. Intro

### 1.1 分析

**Scenario**

- 需要哪些功能？

- qps 多少（可能通过 dau 估算）？

**Service**

- 分而治之，拆解为小服务

**Storage**

- 数据如何存储与访问？
- 系统 = 服务 + 存储

**Scale**

- 解决缺陷，可能遇到的问题

## 2. Feed

### 2.1 Pull

**流程**

1. request
2. get the followings
3. get tweets from followings
4. merge, return

**复杂度**

读：n 次 io（n 为好友数量）

写：1 次 io

### 2.2 Push

- Pull vs Push
- 什么是 mq?
- 什么是 persistent?
- 什么是 denormalize?
- 什么是 thundering hard?