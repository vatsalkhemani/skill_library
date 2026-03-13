---
name: mcp-builder
description: Guide for creating high-quality MCP (Model Context Protocol) servers that enable LLMs to interact with external services through well-designed tools. Use when building MCP servers to integrate external APIs or services, whether in Python (FastMCP) or Node/TypeScript (MCP SDK).
---

# MCP Server Development Guide

## Overview

Create MCP (Model Context Protocol) servers that enable LLMs to interact with external services through well-designed tools. The quality of an MCP server is measured by how well it enables LLMs to accomplish real-world tasks.

---

## Process

### Phase 1: Deep Research and Planning

#### 1.1 Understand Modern MCP Design

**API Coverage vs. Workflow Tools:**
Balance comprehensive API endpoint coverage with specialized workflow tools. When uncertain, prioritize comprehensive API coverage.

**Tool Naming and Discoverability:**
Use consistent prefixes (e.g., `github_create_issue`, `github_list_repos`) and action-oriented naming.

**Context Management:**
Design tools that return focused, relevant data. Support filtering and pagination.

**Actionable Error Messages:**
Error messages should guide agents toward solutions with specific suggestions and next steps.

#### 1.2 Study MCP Protocol Documentation

Start with the sitemap: `https://modelcontextprotocol.io/sitemap.xml`
Fetch specific pages with `.md` suffix (e.g., `https://modelcontextprotocol.io/specification/draft.md`).

Key pages to review:
- Specification overview and architecture
- Transport mechanisms (streamable HTTP, stdio)
- Tool, resource, and prompt definitions

#### 1.3 Choose Your Stack

**Recommended:** TypeScript (best SDK support, broad compatibility, good AI code generation)
**Transport:** Streamable HTTP for remote servers (stateless JSON), stdio for local servers.

**SDK Documentation:**
- **TypeScript SDK**: `https://raw.githubusercontent.com/modelcontextprotocol/typescript-sdk/main/README.md`
- **Python SDK**: `https://raw.githubusercontent.com/modelcontextprotocol/python-sdk/main/README.md`

---

### Phase 2: Implementation

#### 2.1 Project Structure

See language-specific SDK guides for project setup.

#### 2.2 Core Infrastructure

Create shared utilities:
- API client with authentication
- Error handling helpers
- Response formatting (JSON/Markdown)
- Pagination support

#### 2.3 Implement Tools

For each tool:

**Input Schema:** Use Zod (TypeScript) or Pydantic (Python) with constraints and clear descriptions.

**Output Schema:** Define `outputSchema` where possible. Use `structuredContent` in responses.

**Tool Description:** Concise summary, parameter descriptions, return type schema.

**Implementation:**
- Async/await for I/O operations
- Proper error handling with actionable messages
- Support pagination where applicable

**Annotations:**
- `readOnlyHint`: true/false
- `destructiveHint`: true/false
- `idempotentHint`: true/false
- `openWorldHint`: true/false

---

### Phase 3: Review and Test

**Code Quality:** No duplicated code, consistent error handling, full type coverage, clear tool descriptions.

**Build and Test:**
- TypeScript: `npm run build` then `npx @modelcontextprotocol/inspector`
- Python: `python -m py_compile your_server.py` then MCP Inspector

---

### Phase 4: Create Evaluations

Create 10 evaluation questions to test whether LLMs can effectively use your MCP server.

**Requirements for each question:**
- Independent (not dependent on other questions)
- Read-only (non-destructive operations only)
- Complex (requires multiple tool calls)
- Realistic (based on real use cases)
- Verifiable (single, clear answer)
- Stable (answer won't change over time)

**Output format:**
```xml
<evaluation>
  <qa_pair>
    <question>Your question here</question>
    <answer>Expected answer</answer>
  </qa_pair>
</evaluation>
```
