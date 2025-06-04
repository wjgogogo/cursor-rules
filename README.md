# Cursor Rules

一套完整的前端开发规范和最佳实践，专为 Cursor AI 编程助手设计。

## 项目简介

本项目提供了一套标准化的开发规范，涵盖代码质量、命名规范、技术栈选型、性能优化等各个方面。这些规则旨在提高代码质量、团队协作效率和项目可维护性。

## 规则概览

### 📋 核心规范
- **[代码质量规范](/.cursor/rules/code-quality.mdc)** - 代码示例要求、质量标准和检查清单
- **[命名规范](/.cursor/rules/naming-conventions.mdc)** - 文件、变量、函数、组件的命名约定
- **[模块导出规范](/.cursor/rules/module-exports.mdc)** - 模块导入导出的最佳实践

### 🛠️ 技术栈规范
- **[技术栈选型规范](/.cursor/rules/tech-stack.mdc)** - 核心技术栈和选型原则
- **[React 开发规范](/.cursor/rules/react-standards.mdc)** - React 组件、Hooks 和编程模式
- **[TypeScript 规范](/.cursor/rules/typescript-standards.mdc)** - 类型定义和类型安全最佳实践
- **[样式规范](/.cursor/rules/styling-standards.mdc)** - Tailwind CSS 和 shadcn/ui 使用规范

### 🚀 性能与工具
- **[性能优化规范](/.cursor/rules/performance-optimization.mdc)** - React 应用性能优化最佳实践
- **[npm 包安装规范](/.cursor/rules/install-package.mdc)** - 包管理和 monorepo 工作区管理

### 📝 文档与协作
- **[文档书写规范](/.cursor/rules/docs-guide.mdc)** - Markdown 格式和文档编写标准
- **[Git 提交消息规范](/.cursor/rules/git-commit-message.mdc)** - 提交消息格式和分支管理

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
@code-quality 检查我的代码质量
@naming-conventions 帮我优化变量命名
@react-standards 这个组件是否符合规范？
```

## 规则详细说明

### 代码质量规范 (`code-quality.mdc`)

确保代码示例的可执行性和质量标准：
- **代码示例要求**：语法正确、包含完整导入、TypeScript 类型准确
- **质量要求**：正确性、时效性、功能完整、安全性、可读性优先
- **完整性原则**：禁止 TODO、功能缺失，必须引用具体文件名
- **质量工具**：ESLint、Prettier、TypeScript、Husky + lint-staged

### 命名规范 (`naming-conventions.mdc`)

统一的命名约定和风格指南：
- **文件命名**：使用 `kebab-case`
- **变量命名**：`camelCase`、`PascalCase`、`UPPER_SNAKE_CASE`
- **布尔值命名**：使用 `is`、`has`、`can`、`should` 前缀
- **函数命名**：动词开头，描述行为
- **组件和 Props**：直观反映用途
- **Hooks 命名**：以 `use` 开头

### 技术栈选型规范 (`tech-stack.mdc`)

核心技术栈和选型原则：
- **核心技术**：React + TypeScript、Tailwind CSS + shadcn/ui、Zustand、React Router、Vite
- **选型原则**：稳定性、社区活跃、性能影响、团队熟悉度、长期维护
- **版本管理**：定期更新、语义化版本、充分测试、保持一致性

### React 开发规范 (`react-standards.mdc`)

React 开发的最佳实践：
- **组件定义**：函数组件 + Hooks、TypeScript 类型、命名导出
- **Hooks 使用**：以 `use` 开头、不在条件语句中使用、复杂逻辑封装
- **编程模式**：函数式和声明式、描述性变量名、迭代和模块化

### TypeScript 规范 (`typescript-standards.mdc`)

TypeScript 类型定义和安全实践：
- **类型定义**：为所有变量定义类型、优先使用 `interface`、禁止 `enum`
- **导出类型**：`.d.ts` 文件、共享类型、组件特定类型
- **类型安全**：避免 `any`、严格配置、类型守卫、泛型复用

### 样式规范 (`styling-standards.mdc`)

Tailwind CSS 和 shadcn/ui 使用规范：
- **Tailwind CSS**：原子类优先、`@apply` 指令、移动优先响应式设计
- **shadcn/ui**：作为 UI 基础、遵循文档、Tailwind 微调
- **主题和暗模式**：`dark:` 前缀、CSS 变量、设计系统
- **响应式原则**：移动优先、设备可用性

### 性能优化规范 (`performance-optimization.mdc`)

React 应用性能优化最佳实践：
- **Suspense 和错误边界**：提供 fallback
- **动态加载**：非关键组件懒加载
- **内存优化**：清理副作用、防止内存泄漏
- **渲染优化**：React.memo、useMemo、useCallback
- **网络优化**：请求去重
- **用户交互优化**：防抖实现
- **代码分割**：按路由分割

### npm 包安装规范 (`install-package.mdc`)

包管理和 monorepo 工作区管理：
- **安装要求**：优先 pnpm、锁定版本、全局依赖说明
- **Monorepo 管理**：工作区配置、依赖安装策略、版本管理
- **内部包引用**：workspace 协议
- **常用命令**：安装、运行、清理

### 文档书写规范 (`docs-guide.mdc`)

Markdown 格式和文档编写标准：
- **Markdown 格式**：标题层级、列表、代码块、表格
- **中英文排版**：空格、标点、字符规范
- **语言风格**：中文编写、短句优先、删除累赘词
- **代码示例**：语法正确、可运行、类型完整
- **文档更新**：同步更新、版本标注

### Git 提交消息规范 (`git-commit-message.mdc`)

提交消息格式和分支管理：
- **格式要求**：`<类型>: <简短描述>`
- **类型标识**：feat、fix、docs、style、refactor、perf、test、chore
- **描述规范**：中文、50 字符内、动词开头、现在时
- **分支管理**：main、feat/、fix/ 分支
- **提交前检查**：测试通过、消息规范、相关更改

### Context7 MCP 集成规范 (`context7.mdc`)

第三方库文档获取流程：
- **使用要求**：首次引入/升级必须通过 Context7 MCP 获取文档
- **流程**：resolve-library-id → get-library-docs → 按文档实现
- **示例**：axios 库的正确使用流程

### LLM 严格模式规则 (`llm.mdc`)

AI 编程助手的工作模式约束：
- **模式声明**：每次回复声明当前模式
- **各模式约束**：RESEARCH、INNOVATE、PLAN、EXECUTE、REVIEW
- **切换信号**：仅在明确信号时切换
- **偏离处理**：发现偏离立即返回 PLAN 模式

