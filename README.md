# Doc Master Skill

[English](#english) | [中文](#中文)

---

<a name="english"></a>
## English

Advanced documentation analysis and content generation skill for Claude Code.

### Overview

Doc Master enhances Claude's ability to analyze, understand, and synthesize information from diverse documentation sources. It provides systematic workflows for deep document analysis, cross-document synthesis, knowledge graph construction, and structured content generation.

### Key Features

- **Multi-Source Document Acquisition**: Retrieve documents from local files, web resources, and library documentation
- **Intelligent Document Understanding**: Systematic analysis with structure recognition, content extraction, and semantic understanding
- **Cross-Document Synthesis**: Correlate information across multiple sources with comparative analysis
- **Knowledge Graph Construction**: Build structured knowledge using memory tools for persistent learning
- **Structured Content Generation**: Produce high-quality analytical outputs using proven templates

### Installation

#### For Claude Code Users

1. Download the skill package
2. Extract to your Claude skills directory:
   ```bash
   unzip doc-master.zip -d ~/.claude/skills/
   ```
3. Restart Claude Code or reload skills

#### For GitHub Users

Clone this repository and place it in your Claude skills directory:

```bash
git clone https://github.com/cookiesen77-rgb/doc-master.git ~/.claude/skills/doc-master
```

### Usage Examples

#### Analyze Technical Documentation

```
Analyze the FastAPI documentation and explain how to build a REST API
```

The skill will:
- Fetch FastAPI documentation using Context7
- Extract core concepts (routes, dependencies, models)
- Identify patterns and best practices
- Generate a tutorial-style guide with code examples

#### Compare Multiple Frameworks

```
Compare React, Vue, and Svelte for my project
```

The skill will:
- Fetch documentation for all frameworks in parallel
- Build a comparison matrix
- Analyze trade-offs for your specific use case
- Provide recommendations with rationale

#### Understand Codebase Architecture

```
Understand the architecture of this codebase
```

The skill will:
- Discover key files using pattern matching
- Find architectural patterns and conventions
- Read critical files to understand structure
- Build a knowledge graph of components
- Generate an architecture overview document

#### Extract API Information

```
Extract all API endpoints from this OpenAPI spec
```

The skill will:
- Read the OpenAPI specification
- Parse and extract endpoint definitions
- Create knowledge graph entities
- Generate a structured API reference

### How It Works

Doc Master uses a systematic approach to document analysis:

1. **Acquisition**: Selects optimal tools (Read, Glob, Grep, WebFetch, Context7) based on document source
2. **Analysis**: Applies structure recognition, content extraction, and semantic understanding
3. **Synthesis**: Correlates information across sources when multiple documents are involved
4. **Knowledge Building**: Creates persistent knowledge graphs using memory tools
5. **Generation**: Produces structured outputs using proven templates

### Workflow Patterns

The skill supports four main workflow patterns:

- **Single Document Deep Dive**: Comprehensive analysis of one document
- **Multi-Document Synthesis**: Comparative analysis across multiple sources
- **Exploratory Research**: Iterative discovery and analysis of related documents
- **API Documentation Mastery**: Specialized workflow for API documentation

### Output Formats

Doc Master generates structured outputs including:

- **Technical Documentation Analysis**: Executive summary, core concepts, key components, code examples
- **Comparative Analysis**: Source comparison matrix, consensus findings, contradictions, synthesis
- **Knowledge Extraction**: Concept hierarchy, entity catalog, relationship graph, insights

### Best Practices

The skill follows these principles:

- **Efficiency**: Parallel tool execution, targeted queries, smart caching
- **Accuracy**: Cross-referencing, confidence levels, source attribution
- **Completeness**: Following reference chains, version checking, gap identification
- **Usability**: Scannable structure, actionable recommendations, source links

### Advanced Techniques

- **Semantic Chunking**: Process large documents in logical sections
- **Progressive Refinement**: Quick scans followed by deep dives
- **Context-Aware Extraction**: Tailored strategies for different document types
- **Knowledge Graph Querying**: Answer questions without re-reading documents
- **Multi-Modal Analysis**: Handle diagrams, tables, and code appropriately

### Requirements

This skill leverages Claude Code's built-in tools:

- Read, Glob, Grep for local file operations
- WebFetch, WebSearch for web resources
- Context7 MCP server for library documentation
- Memory MCP server for knowledge graph construction

No additional dependencies required.

### Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

### License

MIT License - feel free to use and modify as needed.

---

<a name="中文"></a>
## 中文

Claude Code 的高级文档分析和内容生成技能。

### 概述

Doc Master 增强了 Claude 分析、理解和综合来自不同文档源信息的能力。它提供了深度文档分析、跨文档综合、知识图谱构建和结构化内容生成的系统化工作流程。

### 核心功能

- **多源文档获取**：从本地文件、网络资源和库文档中检索文档
- **智能文档理解**：通过结构识别、内容提取和语义理解进行系统分析
- **跨文档综合**：通过对比分析关联多个来源的信息
- **知识图谱构建**：使用记忆工具构建结构化知识以实现持久学习
- **结构化内容生成**：使用经过验证的模板生成高质量分析输出

### 安装方法

#### Claude Code 用户

1. 下载技能包
2. 解压到 Claude 技能目录：
   ```bash
   unzip doc-master.zip -d ~/.claude/skills/
   ```
3. 重启 Claude Code 或重新加载技能

#### GitHub 用户

克隆此仓库并放置到 Claude 技能目录：

```bash
git clone https://github.com/cookiesen77-rgb/doc-master.git ~/.claude/skills/doc-master
```

### 使用示例

#### 分析技术文档

```
分析 FastAPI 文档并解释如何构建 REST API
```

该技能将：
- 使用 Context7 获取 FastAPI 文档
- 提取核心概念（路由、依赖、模型）
- 识别模式和最佳实践
- 生成带代码示例的教程式指南

#### 对比多个框架

```
对比 React、Vue 和 Svelte，看哪个适合我的项目
```

该技能将：
- 并行获取所有框架的文档
- 构建对比矩阵
- 分析针对你特定用例的权衡
- 提供带理由的推荐

#### 理解代码库架构

```
理解这个代码库的架构
```

该技能将：
- 使用模式匹配发现关键文件
- 查找架构模式和约定
- 读取关键文件以理解结构
- 构建组件知识图谱
- 生成架构概览文档

#### 提取 API 信息

```
从这个 OpenAPI 规范中提取所有 API 端点
```

该技能将：
- 读取 OpenAPI 规范
- 解析并提取端点定义
- 创建知识图谱实体
- 生成结构化 API 参考

### 工作原理

Doc Master 使用系统化方法进行文档分析：

1. **获取**：根据文档来源选择最优工具（Read、Glob、Grep、WebFetch、Context7）
2. **分析**：应用结构识别、内容提取和语义理解
3. **综合**：当涉及多个文档时关联来源信息
4. **知识构建**：使用记忆工具创建持久化知识图谱
5. **生成**：使用经过验证的模板生成结构化输出

### 工作流模式

该技能支持四种主要工作流模式：

- **单文档深度分析**：对单个文档进行全面分析
- **多文档综合**：跨多个来源的对比分析
- **探索性研究**：迭代发现和分析相关文档
- **API 文档精通**：专门针对 API 文档的工作流

### 输出格式

Doc Master 生成的结构化输出包括：

- **技术文档分析**：执行摘要、核心概念、关键组件、代码示例
- **对比分析**：来源对比矩阵、共识发现、矛盾点、综合结论
- **知识提取**：概念层次、实体目录、关系图谱、洞察

### 最佳实践

该技能遵循以下原则：

- **效率**：并行工具执行、针对性查询、智能缓存
- **准确性**：交叉引用、置信度级别、来源归属
- **完整性**：跟踪引用链、版本检查、差距识别
- **可用性**：可扫描结构、可操作建议、来源链接

### 高级技术

- **语义分块**：在逻辑部分处理大型文档
- **渐进式精炼**：快速扫描后进行深度分析
- **上下文感知提取**：针对不同文档类型的定制策略
- **知识图谱查询**：无需重新阅读文档即可回答问题
- **多模态分析**：适当处理图表、表格和代码

### 要求

该技能利用 Claude Code 的内置工具：

- Read、Glob、Grep 用于本地文件操作
- WebFetch、WebSearch 用于网络资源
- Context7 MCP 服务器用于库文档
- Memory MCP 服务器用于知识图谱构建

无需额外依赖。

### 贡献

欢迎贡献！请随时提交问题或拉取请求。

### 许可证

MIT 许可证 - 可自由使用和修改。
