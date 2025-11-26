# Doc Master Skill

Advanced documentation analysis and content generation skill for Claude Code.

## Overview

Doc Master enhances Claude's ability to analyze, understand, and synthesize information from diverse documentation sources. It provides systematic workflows for deep document analysis, cross-document synthesis, knowledge graph construction, and structured content generation.

## Key Features

- **Multi-Source Document Acquisition**: Retrieve documents from local files, web resources, and library documentation
- **Intelligent Document Understanding**: Systematic analysis with structure recognition, content extraction, and semantic understanding
- **Cross-Document Synthesis**: Correlate information across multiple sources with comparative analysis
- **Knowledge Graph Construction**: Build structured knowledge using memory tools for persistent learning
- **Structured Content Generation**: Produce high-quality analytical outputs using proven templates

## Installation

### For Claude Code Users

1. Download the skill package
2. Extract to your Claude skills directory:
   ```bash
   unzip doc-master.zip -d ~/.claude/skills/
   ```
3. Restart Claude Code or reload skills

### For GitHub Users

Clone or download this repository and place it in your Claude skills directory:

```bash
git clone https://github.com/YOUR_USERNAME/doc-master.git ~/.claude/skills/doc-master
```

## Usage Examples

### Analyze Technical Documentation

```
Analyze the FastAPI documentation and explain how to build a REST API
```

The skill will:
- Fetch FastAPI documentation using Context7
- Extract core concepts (routes, dependencies, models)
- Identify patterns and best practices
- Generate a tutorial-style guide with code examples

### Compare Multiple Frameworks

```
Compare React, Vue, and Svelte for my project
```

The skill will:
- Fetch documentation for all frameworks in parallel
- Build a comparison matrix
- Analyze trade-offs for your specific use case
- Provide recommendations with rationale

### Understand Codebase Architecture

```
Understand the architecture of this codebase
```

The skill will:
- Discover key files using pattern matching
- Find architectural patterns and conventions
- Read critical files to understand structure
- Build a knowledge graph of components
- Generate an architecture overview document

### Extract API Information

```
Extract all API endpoints from this OpenAPI spec
```

The skill will:
- Read the OpenAPI specification
- Parse and extract endpoint definitions
- Create knowledge graph entities
- Generate a structured API reference

## How It Works

Doc Master uses a systematic approach to document analysis:

1. **Acquisition**: Selects optimal tools (Read, Glob, Grep, WebFetch, Context7) based on document source
2. **Analysis**: Applies structure recognition, content extraction, and semantic understanding
3. **Synthesis**: Correlates information across sources when multiple documents are involved
4. **Knowledge Building**: Creates persistent knowledge graphs using memory tools
5. **Generation**: Produces structured outputs using proven templates

## Workflow Patterns

The skill supports four main workflow patterns:

- **Single Document Deep Dive**: Comprehensive analysis of one document
- **Multi-Document Synthesis**: Comparative analysis across multiple sources
- **Exploratory Research**: Iterative discovery and analysis of related documents
- **API Documentation Mastery**: Specialized workflow for API documentation

## Output Formats

Doc Master generates structured outputs including:

- **Technical Documentation Analysis**: Executive summary, core concepts, key components, code examples
- **Comparative Analysis**: Source comparison matrix, consensus findings, contradictions, synthesis
- **Knowledge Extraction**: Concept hierarchy, entity catalog, relationship graph, insights

## Best Practices

The skill follows these principles:

- **Efficiency**: Parallel tool execution, targeted queries, smart caching
- **Accuracy**: Cross-referencing, confidence levels, source attribution
- **Completeness**: Following reference chains, version checking, gap identification
- **Usability**: Scannable structure, actionable recommendations, source links

## Advanced Techniques

- **Semantic Chunking**: Process large documents in logical sections
- **Progressive Refinement**: Quick scans followed by deep dives
- **Context-Aware Extraction**: Tailored strategies for different document types
- **Knowledge Graph Querying**: Answer questions without re-reading documents
- **Multi-Modal Analysis**: Handle diagrams, tables, and code appropriately

## Requirements

This skill leverages Claude Code's built-in tools:

- Read, Glob, Grep for local file operations
- WebFetch, WebSearch for web resources
- Context7 MCP server for library documentation
- Memory MCP server for knowledge graph construction

No additional dependencies required.

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

## License

MIT License - feel free to use and modify as needed.

## Author

Created for the Claude Code community to enhance documentation analysis capabilities.
