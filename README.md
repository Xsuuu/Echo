# 回声

「回声」是一款让用户以“偶像”身份与 AI 粉丝互动的陪伴型应用。用户可以发布动态、收到 AI 粉丝评论、进入粉丝群聊，并逐步形成可持续的陪伴关系。

## 当前阶段

当前处于阶段 00：仓库和协作基础。

已完成或准备中的内容：

- 项目规划、技术栈、页面功能和阶段计划文档。
- `master` 和 `develop` 长期分支。
- App、服务端、后台和文档目录。
- `.gitignore` 和 `.env.example`。
- PR 模板和测试记录模板。

## 目录结构

```text
.
├── 代码存放处/
│   ├── app/        # Flutter App
│   ├── server/     # Node.js 服务端
│   └── admin/      # Vue 3 + TypeScript 管理后台
├── 文档/
│   ├── 协作规范/
│   ├── 测试记录/
│   ├── 回声-App与管理后台页面功能说明.md
│   ├── 回声-分阶段开发与GitHub分支计划.md
│   ├── 回声-技术栈说明.md
│   └── 回声-竞品与用户需求调研.md
├── .env.example
├── .gitignore
└── README.md
```

## 技术栈

- App：Flutter
- 服务端：Node.js
- 主数据库：PostgreSQL
- 缓存与异步：Redis，按需接入
- 管理后台：Vue 3 + TypeScript
- AI：独立 AI 服务层，由服务端统一调度

## 分支规则

长期分支：

```text
master
develop
```

功能分支从 `develop` 创建，命名格式：

```text
feature/阶段编号-中文模块-中文功能
```

修复分支从 `develop` 创建，命名格式：

```text
fix/阶段编号-中文问题
```

## 开发流程

```text
从 develop 创建功能分支
→ 完成功能开发
→ 补充或更新测试记录
→ 提交 PR 到 develop
→ 验收通过后合并
→ 稳定版本再从 develop 合并到 master
```

## 环境配置

复制 `.env.example` 为本地 `.env` 后再填写真实配置。

真实密钥、数据库密码、AI Key、对象存储密钥等敏感信息不能提交到仓库。

## 测试记录

每个功能分支完成后，在 `文档/测试记录/` 下新增一份测试记录。模板见：

```text
文档/测试记录/测试记录模板.md
```
