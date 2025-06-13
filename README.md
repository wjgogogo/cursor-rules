# Cursor Rules

一套精简的前端开发规范，专为 Cursor AI 编程助手设计。

## 项目简介

本项目提供了一套核心开发规范，涵盖代码质量、命名约定、技术栈选型、性能优化、安全防护等方面。这些规则旨在提高代码质量和开发效率。

## 规则概览

### 📋 核心规范
- **[命名规范](/.cursor/rules/naming-conventions.mdc)** - 统一的文件、变量、函数、组件命名约定
- **[模块导出规范](/.cursor/rules/module-exports.mdc)** - 导入导出的最佳实践和循环依赖避免
- **[AI 任务管理规范](/.cursor/rules/task-master.mdc)** - 引入 AI 驱动的任务拆解与进度管理规范

### 🛠️ 技术栈规范
- **[技术栈选型规范](/.cursor/rules/tech-stack.mdc)** - React 18+ + TypeScript 5+ + Vite + Tailwind + shadcn/ui
- **[React 开发规范](/.cursor/rules/react-standards.mdc)** - 函数组件、Hooks 和最佳编程实践
- **[TypeScript 规范](/.cursor/rules/typescript-standards.mdc)** - 类型定义和类型安全实践
- **[样式规范](/.cursor/rules/styling-standards.mdc)** - Tailwind CSS 和 shadcn/ui 使用规范

### 🚀 性能与质量
- **[性能优化规范](/.cursor/rules/performance-optimization.mdc)** - Web Vitals 监控和核心优化技术
- **[测试规范](/.cursor/rules/testing-standards.mdc)** - 测试金字塔和测试最佳实践
- **[错误处理规范](/.cursor/rules/error-handling.mdc)** - 统一错误处理和用户体验

### 🔒 安全与 API
- **[安全规范](/.cursor/rules/security-standards.mdc)** - 输入验证、XSS/CSRF 防护
- **[API 设计规范](/.cursor/rules/api-design.mdc)** - RESTful API 设计和错误处理

### 📦 工具与协作
- **[npm 包安装规范](/.cursor/rules/install-package.mdc)** - 包管理规范
- **[文档书写规范](/.cursor/rules/docs-guide.mdc)** - Markdown 格式和文档编写标准
- **[Git 提交消息规范](/.cursor/rules/git-commit-message.mdc)** - 提交消息格式约定

### 🤖 AI 辅助开发
- **[Context7 MCP 集成规范](/.cursor/rules/context7.mdc)** - 第三方库文档获取流程
- **[LLM 严格模式规则](/.cursor/rules/llm.mdc)** - AI 编程助手的工作模式约束

## 使用方法

### 在 Cursor 中使用

1. 将此项目克隆到本地
2. 在 Cursor 中打开项目
3. 规则会自动被 Cursor AI 识别和应用
4. 在对话中使用 `@规则名` 引用特定规则

### 引用规则示例

```
@naming-conventions 帮我优化变量命名
@react-standards 这个组件是否符合规范？
@security-standards 检查安全漏洞
@performance-optimization 优化页面性能
@api-design 设计 RESTful API
```

## 核心规范说明

### 命名规范
- **文件命名**：`kebab-case`
- **变量函数**：`camelCase`
- **类型组件**：`PascalCase`
- **常量**：`UPPER_SNAKE_CASE`
- **布尔值**：使用 `is/has/can/should` 前缀
- **Hooks**：以 `use` 开头

### 技术栈
- **核心**：React 18+ + TypeScript 5+ + Vite 5+
- **UI**：Tailwind CSS + shadcn/ui
- **状态**：Zustand（中大型项目）/ React Context（小型项目）
- **表单**：React Hook Form + Zod
- **路由**：React Router 6+

### React 开发
- **组件**：函数组件 + Hooks
- **类型**：TypeScript 严格模式 + 完整类型定义
- **导出**：命名导出优于默认导出
- **性能**：React.memo、useMemo、useCallback 合理使用

### 错误处理
- **统一错误类型**：`type | code | message | timestamp`
- **分层处理**：组件级 → 页面级 → 应用级
- **API 错误**：统一 fetch 包装和错误处理
- **用户体验**：友好错误提示

### 性能优化
- **Web Vitals**：LCP、FID、CLS 监控
- **图片优化**：响应式图片、懒加载
- **代码分割**：React.lazy、动态导入
- **用户交互**：防抖、节流

### 安全防护
- **输入验证**：Zod 验证所有用户输入
- **XSS 防护**：DOMPurify 清理 HTML
- **CSRF 防护**：Token 验证
- **敏感数据**：安全存储和传输

### API 设计
- **RESTful**：标准 HTTP 方法和状态码
- **统一响应**：`{ success, data?, error?, message? }`
- **错误处理**：标准化错误码和消息
- **验证**：Zod schema 验证请求

## 🔍 最佳实践

### 开发流程
1. 遵循命名规范创建文件和目录
2. 使用 TypeScript 严格模式
3. 通过 Context7 MCP 获取第三方库文档
4. 实现统一错误处理
5. 编写必要的测试用例
6. 遵循 Git 提交消息规范

### 代码质量
- 所有变量和函数都有明确类型
- 所有错误都有适当处理
- 所有组件都有合理的性能优化
- 所有 API 调用都有超时和重试
- 所有用户输入都有验证

### 团队协作
- 统一的代码风格和规范
- 清晰的提交消息和分支管理
- 完整的文档和注释
- 标准化的错误处理和日志记录

## AI 任务管理规范

本项目引入 AI 驱动的任务拆解与进度管理规范，详见 [task-master.mdc](./.cursor/rules/task-master.mdc)。

### 核心原则
- 智能任务拆解：支持自然语言需求自动分解为可执行任务，层次化、依赖清晰
- 实时进度跟踪：任务状态自动更新，进度可视化，所有变更实时同步到 `task.md`
- AI 辅助执行：为每个任务提供实现指导、代码建议、阻塞解决方案

### 任务文档格式（task.md）
- 标准 Markdown 结构，包含项目概览、任务分解、进度统计、里程碑、每日工作流等
- 任务分为 P0（核心）、P1（重要）、P2（一般）、PX（创新）四级，状态流转清晰
- 每个任务需有描述、验收标准、技术要点、工时、依赖、状态、最后更新时间
- 支持 <details> 展开实现指导、代码示例、注意事项

### 工作流程与最佳实践
- 每日优先处理 P0 任务，实时更新状态，记录进展与阻塞
- 任务拆解需原子、可测试、时间可控、依赖明确
- 定期回顾任务优先级与进度，保持 task.md 文档准确
- 敏感信息不得写入任务描述，注意文档体积与安全

### task.md 模板片段
```markdown
# 项目任务管理

> 📊 **项目进度**: !@进度条
> 🕒 **最后更新**: 2025-01-12 14:30:00
> 📈 **总体状态**: 进行中

## 📑 项目概览
### 需求描述
[项目的核心需求和目标描述]
### 技术栈
- 前端: [技术栈]
- 后端: [技术栈]
- 数据库: [技术栈]
- 其他: [相关技术]

---

## 🎯 任务分解
### P0 - 核心功能 (高优先级 - 立即执行)
#### 任务组 1: [功能模块名称]
- [ ] **T001** - [任务标题] `🔥 P0`
  - **描述**: [详细描述]
  - **验收标准**: [明确的验收标准]
  - **技术要点**: [关键技术点]
  - **预估工时**: [时间估计]
  - **依赖**: [前置任务ID]
  - **状态**: `📋 待开始` | `🔄 进行中` | `✅ 已完成` | `🚫 已阻塞`
  - **最后更新**: [时间戳]

  <details>
  <summary>📝 实现指导</summary>

  **步骤分解**:
  1. [具体步骤1]
  2. [具体步骤2]
  3. [具体步骤3]

  **代码示例**:
  ```javascript
  // 示例代码
  ```  
  **注意事项**:
  - [重要提醒1]
  - [重要提醒2]
  </details>
```

---

*本项目持续更新，确保规范与最新技术保持同步。*
