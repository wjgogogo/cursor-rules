# Cursor Rules

一套精简的前端开发规范，专为 Cursor AI 编程助手设计。

## 项目简介

本项目提供了一套核心开发规范，涵盖代码质量、命名约定、技术栈选型、性能优化、安全防护等方面。这些规则旨在提高代码质量和开发效率。

## 规则概览

### 📋 核心规范
- **[命名规范](/.cursor/rules/naming-conventions.mdc)** - 统一的文件、变量、函数、组件命名约定
- **[模块导出规范](/.cursor/rules/module-exports.mdc)** - 导入导出的最佳实践和循环依赖避免

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

---

*本项目持续更新，确保规范与最新技术保持同步。*
