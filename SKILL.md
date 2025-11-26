---
name: doc-master
description: Advanced documentation analysis and content generation skill. Use when analyzing technical documentation, API references, research papers, code repositories, or any complex documents requiring deep understanding, cross-document synthesis, knowledge graph construction, or structured content generation. Handles mixed document types including technical specs, academic papers, code documentation, and business documents.
---

# Doc Master

## Overview

Doc Master provides comprehensive document analysis and intelligent content generation capabilities. Leverage multi-source document retrieval, deep semantic understanding, cross-document correlation analysis, and structured knowledge extraction to transform raw documentation into actionable insights.

## Core Capabilities

### 1. Multi-Source Document Acquisition

Retrieve documents from diverse sources using optimal strategies:

**Local filesystem analysis:**
- Use Read tool for direct file access
- Use Glob for pattern-based file discovery (`**/*.md`, `docs/**/*.txt`)
- Use Grep for content-based searches across codebases

**Web-based documentation:**
- Use WebFetch for HTML documentation and online resources
- Use WebSearch for discovering relevant documentation sources
- Use mcp__fetch__fetch for advanced web content retrieval

**Library documentation:**
- Use mcp__context7__resolve-library-id to identify library documentation
- Use mcp__context7__get-library-docs with mode='code' for API references
- Use mcp__context7__get-library-docs with mode='info' for conceptual guides

**Strategy selection:**
- For known file paths: Read directly
- For exploratory searches: Glob + Grep in parallel
- For API documentation: Context7 tools
- For web resources: WebFetch with targeted prompts

### 2. Intelligent Document Understanding

Apply systematic analysis to extract maximum value:

**Structure recognition:**
- Identify document type (API docs, tutorial, specification, research paper)
- Map hierarchical structure (sections, subsections, code blocks)
- Detect metadata (authors, dates, versions, dependencies)

**Content extraction:**
- Extract key concepts, definitions, and terminology
- Identify code examples, algorithms, and implementations
- Capture relationships between components
- Note prerequisites, dependencies, and constraints

**Semantic analysis:**
- Understand intent and purpose of documentation
- Identify gaps, ambiguities, or contradictions
- Recognize patterns and conventions
- Assess completeness and quality

### 3. Cross-Document Synthesis

Correlate information across multiple documents:

**Parallel document retrieval:**
Execute multiple Read/WebFetch/Grep operations simultaneously to gather comprehensive context efficiently.

**Comparative analysis:**
- Identify overlapping concepts across sources
- Detect contradictions or inconsistencies
- Find complementary information
- Synthesize unified understanding

**Relationship mapping:**
- Track dependencies between documents
- Map concept hierarchies across sources
- Identify authoritative vs supplementary sources
- Build comprehensive mental model

### 4. Knowledge Graph Construction

Transform documentation into structured knowledge using memory tools:

**Entity creation:**
Use mcp__memory__create_entities to capture:
- Technical concepts (APIs, classes, functions)
- Technologies (libraries, frameworks, tools)
- Processes (workflows, algorithms, patterns)
- People/Organizations (authors, maintainers, companies)

**Relation mapping:**
Use mcp__memory__create_relations to establish:
- Dependencies ("Library A" depends_on "Library B")
- Implementations ("Class X" implements "Interface Y")
- Hierarchies ("Concept A" is_subtype_of "Concept B")
- Associations ("Tool X" used_by "Framework Y")

**Observation enrichment:**
Use mcp__memory__add_observations to augment entities with:
- Usage examples and code snippets
- Performance characteristics
- Best practices and gotchas
- Version-specific information

**Knowledge retrieval:**
- Use mcp__memory__search_nodes for semantic queries
- Use mcp__memory__open_nodes for specific entity details
- Use mcp__memory__read_graph for comprehensive overview

### 5. Structured Content Generation

Produce high-quality analytical outputs:

**Analysis templates:**

For technical documentation:
```
# Document Analysis: [Title]

## Executive Summary
[2-3 sentence overview of purpose and key findings]

## Document Metadata
- Type: [API Reference/Tutorial/Specification/etc.]
- Source: [URL or file path]
- Version: [if applicable]
- Last Updated: [if available]

## Core Concepts
[Hierarchical list of main concepts with brief definitions]

## Key Components
[Detailed breakdown of APIs, classes, functions, or major sections]

## Code Examples
[Extracted and annotated code samples]

## Dependencies & Prerequisites
[Required knowledge, libraries, or setup]

## Strengths & Limitations
[What the documentation does well and gaps identified]

## Related Resources
[Links to complementary documentation]
```

For comparative analysis:
```
# Comparative Analysis: [Topic]

## Sources Analyzed
[List of documents with metadata]

## Comparison Matrix
| Aspect | Source A | Source B | Source C |
|--------|----------|----------|----------|
| [Key dimension] | ... | ... | ... |

## Consensus Findings
[Points where all sources agree]

## Contradictions & Conflicts
[Discrepancies between sources with analysis]

## Synthesis
[Unified understanding incorporating all sources]

## Recommendations
[Actionable guidance based on analysis]
```

For knowledge extraction:
```
# Knowledge Extraction: [Domain]

## Concept Hierarchy
[Tree structure of main concepts and subconcepts]

## Entity Catalog
[Comprehensive list of identified entities by type]

## Relationship Graph
[Visual or textual representation of entity relationships]

## Key Insights
[Non-obvious patterns or findings]

## Knowledge Gaps
[Areas requiring additional research]
```

## Workflow Patterns

### Pattern 1: Single Document Deep Dive

1. Acquire document using appropriate tool
2. Perform initial structural analysis
3. Extract entities and create knowledge graph entries
4. Generate comprehensive analysis report
5. Identify related documents for further exploration

### Pattern 2: Multi-Document Synthesis

1. Identify all relevant documents
2. Execute parallel retrieval operations
3. Perform individual document analysis
4. Build unified knowledge graph across sources
5. Generate comparative analysis highlighting synthesis

### Pattern 3: Exploratory Research

1. Start with broad search (WebSearch or Grep)
2. Identify most relevant sources
3. Retrieve and analyze top candidates
4. Follow references to discover additional sources
5. Iteratively expand knowledge graph
6. Produce comprehensive research summary

### Pattern 4: API Documentation Mastery

1. Use Context7 to resolve library ID
2. Fetch both code and info mode documentation
3. Extract API surface (classes, methods, parameters)
4. Capture usage examples and patterns
5. Build knowledge graph of API relationships
6. Generate practical usage guide

## Best Practices

**Efficiency:**
- Execute independent tool calls in parallel
- Use targeted prompts for WebFetch to reduce token usage
- Leverage Grep with appropriate patterns before reading full files
- Cache frequently accessed documentation in knowledge graph

**Accuracy:**
- Cross-reference information across multiple sources
- Note confidence levels for extracted information
- Preserve source attribution for all facts
- Flag ambiguities and contradictions explicitly

**Completeness:**
- Follow reference chains to discover related documentation
- Check for version-specific information
- Identify and fill knowledge gaps systematically
- Validate understanding through code examples

**Usability:**
- Structure outputs for easy scanning and navigation
- Include actionable recommendations
- Provide code examples where relevant
- Link back to original sources for verification

## Advanced Techniques

**Semantic chunking:**
When documents are large, process in logical sections rather than arbitrary chunks. Identify natural boundaries (chapters, major sections) and analyze incrementally.

**Progressive refinement:**
Start with quick scans to build overview, then dive deep into critical sections. Use initial findings to guide deeper analysis.

**Context-aware extraction:**
Tailor extraction strategy to document type. API docs need different treatment than research papers or tutorials.

**Knowledge graph querying:**
After building knowledge graph, use search_nodes to answer specific questions without re-reading documents.

**Multi-modal analysis:**
For documents with diagrams, tables, or code, ensure all modalities are captured and analyzed appropriately.

## Example Usage Scenarios

**Scenario: "Analyze the FastAPI documentation and explain how to build a REST API"**
1. Use Context7 to fetch FastAPI documentation (both modes)
2. Extract core concepts (routes, dependencies, models)
3. Identify key patterns and best practices
4. Generate tutorial-style guide with code examples

**Scenario: "Compare React, Vue, and Svelte for my project"**
1. Fetch documentation for all three frameworks in parallel
2. Build comparison matrix (learning curve, performance, ecosystem)
3. Analyze trade-offs for specific use case
4. Provide recommendation with rationale

**Scenario: "Understand the architecture of this codebase"**
1. Use Glob to discover key files (README, architecture docs, main source files)
2. Use Grep to find architectural patterns and conventions
3. Read critical files to understand structure
4. Build knowledge graph of components and relationships
5. Generate architecture overview document

**Scenario: "Extract all API endpoints from this OpenAPI spec"**
1. Read OpenAPI specification file
2. Parse and extract endpoint definitions
3. Create knowledge graph entities for each endpoint
4. Generate structured API reference document

## Resources

This skill leverages all available tools for maximum capability. No additional scripts, references, or assets are required - the skill's power comes from intelligent orchestration of existing tools and systematic application of analysis frameworks.
