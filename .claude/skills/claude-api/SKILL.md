---
name: claude-api
description: Build apps with the Claude API or Anthropic SDK. TRIGGER when code imports `anthropic`/`@anthropic-ai/sdk`/`claude_agent_sdk`, or user asks to use Claude API, Anthropic SDKs, or Agent SDK. DO NOT TRIGGER when code imports `openai`/other AI SDK, general programming, or ML/data-science tasks.
---

# Claude API & Agent SDK Skill

## Key Defaults

- **Model:** Use `claude-opus-4-6` unless explicitly told otherwise
- **Thinking:** Apply `thinking: {type: "adaptive"}` for complex tasks (no deprecated `budget_tokens`)
- **Streaming:** Default to streaming for long inputs/outputs to prevent timeouts

## Language Detection Workflow

Identify the project language from file extensions and config files (`.py`, `package.json`, `go.mod`, etc.), then read language-specific documentation from the appropriate folder.

## Surface Selection

Choose based on task complexity:
- **Single API call** → Claude API (classification, summarization, extraction)
- **Multi-step workflow** → Claude API + tool use
- **Open-ended agent** → Agent SDK (for Python/TypeScript with built-in file/web/terminal tools)

The decision hinges on whether Claude needs autonomous file/web/shell access, complexity justification, and error recovery viability.

## Architecture Essentials

All interactions use `POST /v1/messages`. Tools, structured outputs, and constraints are features of this single endpoint. The SDK's tool runner handles API calls, function execution, and looping automatically.

## Critical Reminders

- Never use `budget_tokens` with Opus 4.6 — use adaptive thinking instead
- Use `output_config: {format: {...}}` for structured outputs (not deprecated `output_format`)
- Preserve compaction blocks when appending responses to conversation history
- Stream for `max_tokens` >100K to avoid timeouts
