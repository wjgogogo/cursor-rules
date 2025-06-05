# Cursor Rules

一套完整的前端开发规范和最佳实践，专为 Cursor AI 编程助手设计。

## 项目简介

本项目提供了一套标准化的开发规范，涵盖代码质量、命名规范、技术栈选型、性能优化、安全防护、测试策略等各个方面。这些规则旨在提高代码质量、团队协作效率和项目可维护性。

## 规则概览

### 📋 核心规范
- **[命名规范](/.cursor/rules/naming-conventions.mdc)** - 文件、变量、函数、组件的命名约定
- **[模块导出规范](/.cursor/rules/module-exports.mdc)** - 模块导入导出的最佳实践

### 🛠️ 技术栈规范
- **[技术栈选型规范](/.cursor/rules/tech-stack.mdc)** - 核心技术栈、工具链配置和选型原则
- **[React 开发规范](/.cursor/rules/react-standards.mdc)** - React 组件、Hooks 和编程模式
- **[TypeScript 规范](/.cursor/rules/typescript-standards.mdc)** - 类型定义、泛型使用和类型安全最佳实践
- **[样式规范](/.cursor/rules/styling-standards.mdc)** - 设计系统、Tailwind CSS 和 shadcn/ui 使用规范

### 🚀 性能与质量
- **[性能优化规范](/.cursor/rules/performance-optimization.mdc)** - Web Vitals 监控、图片优化和性能最佳实践
- **[测试规范](/.cursor/rules/testing-standards.mdc)** - 测试金字塔、单元测试和 E2E 测试策略
- **[错误处理规范](/.cursor/rules/error-handling.mdc)** - 统一错误处理、日志记录和用户体验

### 🔒 安全与 API
- **[安全规范](/.cursor/rules/security-standards.mdc)** - 输入验证、XSS/CSRF 防护和安全最佳实践
- **[API 设计规范](/.cursor/rules/api-design.mdc)** - RESTful API 设计、错误码标准化和性能优化

### 📦 工具与部署
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
@naming-conventions 帮我优化变量命名
@react-standards 这个组件是否符合规范？
@security-standards 检查安全漏洞
@testing-standards 帮我编写测试用例
@api-design 设计 RESTful API
```

## 规则详细说明

### 命名规范 (`naming-conventions.mdc`)

统一的命名约定和风格指南：
- **文件命名**：使用 `kebab-case`
- **变量命名**：`camelCase`、`PascalCase`、`UPPER_SNAKE_CASE`
- **布尔值命名**：使用 `is`、`has`、`can`、`should` 前缀
- **函数命名**：动词开头，描述行为
- **组件和 Props**：直观反映用途
- **Hooks 命名**：以 `use` 开头

### 技术栈选型规范 (`tech-stack.mdc`)

核心技术栈和完整工具链配置：
- **核心技术**：React 18+ + TypeScript 5+、Tailwind CSS 3+ + shadcn/ui、Zustand、React Router 6+、Vite 5+
- **测试框架**：Vitest + Testing Library、Playwright、Storybook
- **构建部署**：Vite + SWC、pnpm、GitHub Actions、Vercel/Netlify
- **开发工具**：ESLint + Prettier + TypeScript、Husky + lint-staged
- **版本兼容性**：详细的版本矩阵和升级策略
- **选型原则**：稳定性、社区活跃、性能影响、团队熟悉度、长期维护

### React 开发规范 (`react-standards.mdc`)

React 开发的最佳实践：
- **组件定义**：函数组件 + Hooks、TypeScript 类型、命名导出
- **Hooks 使用**：以 `use` 开头、不在条件语句中使用、复杂逻辑封装
- **编程模式**：函数式和声明式、描述性变量名、迭代和模块化

### TypeScript 规范 (`typescript-standards.mdc`)

TypeScript 类型定义和安全实践：
- **类型定义**：为所有变量定义类型、优先使用 `interface`、禁止 `enum`
- **泛型使用**：泛型约束、条件类型、映射类型、工具类型组合
- **类型守卫**：基础类型守卫、联合类型守卫、自定义断言函数
- **tsconfig 配置**：严格模式、路径映射、编译优化
- **高级类型**：模板字面量类型、递归类型、品牌类型、状态机类型
- **类型安全**：避免 `any`、严格配置、类型守卫、泛型复用

### 样式规范 (`styling-standards.mdc`)

完整的设计系统和样式规范：
- **设计系统**：颜色系统、字体系统、间距系统、阴影和边框
- **组件变体**：按钮变体、状态样式、尺寸变体
- **Tailwind CSS**：原子类优先、`@apply` 指令、移动优先响应式设计
- **shadcn/ui**：作为 UI 基础、遵循文档、Tailwind 微调
- **可访问性**：焦点管理、颜色对比度、屏幕阅读器支持
- **动画效果**：过渡动画、微交互、性能优化
- **主题和暗模式**：`dark:` 前缀、CSS 变量、设计系统

### 性能优化规范 (`performance-optimization.mdc`)

全面的性能优化策略：
- **Web Vitals 监控**：LCP、FID、CLS、FCP、TTFB 指标监控和优化
- **图片优化**：响应式图片、格式优化（WebP/AVIF）、懒加载
- **Bundle 分析**：Webpack Bundle Analyzer、Tree Shaking、代码分割
- **缓存策略**：HTTP 缓存、Service Worker、内存缓存、React Query 缓存
- **渲染优化**：React.memo、useMemo、useCallback、虚拟滚动
- **网络优化**：请求去重、批处理、超时处理
- **用户交互优化**：防抖、节流
- **性能监控**：性能指标收集、分析和上报

### 测试规范 (`testing-standards.mdc`)

完整的测试策略和最佳实践：
- **测试金字塔**：70% 单元测试、20% 集成测试、10% E2E 测试
- **单元测试**：Vitest + Testing Library、组件测试、Hook 测试、工具函数测试
- **集成测试**：API 集成、组件集成、用户流程测试
- **E2E 测试**：Playwright、关键用户路径、跨浏览器测试
- **测试配置**：测试环境设置、Mock 策略、测试数据管理
- **测试覆盖率**：≥80% 覆盖率要求、关键路径 100% 覆盖
- **CI/CD 集成**：自动化测试、测试报告、失败处理

### 错误处理规范 (`error-handling.mdc`)

统一的错误处理和用户体验：
- **错误分类**：验证错误、网络错误、业务错误、系统错误
- **错误边界**：React 错误边界、功能级错误边界、错误恢复
- **API 错误处理**：统一错误格式、HTTP 状态码、重试机制
- **异步错误处理**：Promise 错误、超时处理、并发错误
- **表单错误处理**：实时验证、错误提示、用户引导
- **日志记录**：分级日志、远程日志、错误上报
- **用户体验**：友好错误提示、错误恢复建议、Toast 通知

### 安全规范 (`security-standards.mdc`)

全面的安全防护体系：
- **输入验证**：Zod 验证、SQL 注入防护、文件上传安全
- **XSS 防护**：内容安全策略、输出编码、DOM 操作安全
- **CSRF 防护**：CSRF Token、SameSite Cookie、双重提交
- **敏感数据处理**：数据加密、安全存储、传输安全
- **API 安全**：认证授权、速率限制、输入验证
- **依赖安全**：漏洞扫描、依赖更新、安全审计
- **安全检查清单**：开发、测试、部署各阶段的安全检查

### API 设计规范 (`api-design.mdc`)

RESTful API 设计和最佳实践：
- **RESTful 设计**：资源导向、HTTP 方法正确使用、URL 设计
- **响应格式**：统一响应结构、分页格式、错误格式
- **状态码规范**：正确使用 HTTP 状态码、错误码标准化
- **输入验证**：Zod 验证、类型安全、错误处理
- **版本控制**：URL 版本控制、向后兼容、版本迁移
- **性能优化**：缓存策略、分页优化、字段选择
- **API 安全**：认证授权、速率限制、输入验证
- **文档生成**：OpenAPI 规范、类型生成、API 文档

### npm 包安装规范 (`install-package.mdc`)

包管理和 monorepo 工作区管理：
- **安装要求**：优先 pnpm、锁定版本、全局依赖说明
- **Monorepo 管理**：工作区配置、依赖安装策略、版本管理
- **内部包引用**：workspace 协议

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
- **强制检查清单**：文档获取、版本确认、最佳实践、类型安全、错误处理、性能优化、可访问性
- **示例**：axios 库的正确使用流程

### LLM 严格模式规则 (`llm.mdc`)

AI 编程助手的工作模式约束：
- **模式声明**：每次回复声明当前模式
- **RIPER-5 模式**：RESEARCH、INNOVATE、PLAN、EXECUTE、REVIEW
- **各模式约束**：明确的权限和禁止事项
- **切换信号**：仅在明确信号时切换
- **偏离处理**：发现偏离立即返回 PLAN 模式
