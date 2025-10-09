# Claude Code 101

A learning repository for getting started with [Claude Code](https://claude.ai/code), Anthropic's official CLI for Claude. This repo serves as a hands-on guide to understanding Claude Code's capabilities, MCP servers, and best practices.

## Table of Contents

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [MCP Servers](#mcp-servers)
- [Learning Path](#learning-path)
- [Resources](#resources)

## Overview

Claude Code is an interactive CLI tool that helps with software engineering tasks. This repository is designed to help you:

- Learn how to effectively use Claude Code
- Understand and configure MCP (Model Context Protocol) servers
- Explore practical examples and workflows
- Build familiarity with AI-assisted development

## Prerequisites

Before getting started, ensure you have:

- [Claude Code](https://docs.claude.com/en/docs/claude-code) installed
- Basic command line knowledge
- Git installed on your system

## Getting Started

1. **Clone this repository:**
   ```bash
   git clone https://github.com/yourusername/claude-code-101.git
   cd claude-code-101
   ```

2. **Initialize Claude Code in your project:**
   ```bash
   claude
   ```

3. **Explore the examples** in this repository to learn different workflows

## MCP Servers

MCP (Model Context Protocol) servers extend Claude Code's capabilities by connecting it to external tools and services (e.g., databases, browsers, file systems, APIs).

### Why Use MCP Servers?

- **Enhanced capabilities**: Access tools beyond Claude's base functionality
- **Efficiency**: Specialized servers can handle tasks more efficiently
- **Extensibility**: Connect Claude to your existing tools and workflows

### Serena MCP Server

**Serena** is a semantic code analysis MCP server that makes Claude Code significantly more efficient when working with codebases. It enables token-efficient code reading through semantic understanding rather than reading entire files.

**Benefits:**
- Reduces token usage by up to 90% when reading code
- Provides semantic code navigation
- Perfect for understanding and working with existing codebases

#### Installing Serena MCP Server

**Step 1:** Install `uv` (Python package manager)
```bash
brew install uv
```

**Step 2:** Add Serena to Claude Code
```bash
claude mcp add serena -- uvx --from git+https://github.com/oraios/serena serena start-mcp-server --context ide-assistant --project $(pwd)
```

**Step 3:** Verify the installation
```bash
claude mcp list
```

You should see `serena` listed among your MCP servers.

**Documentation:** [Serena GitHub Repository](https://github.com/oraios/serena)

### Other Useful MCP Servers

Explore more MCP servers in the [MCP Server Registry](https://github.com/modelcontextprotocol/servers).

## Learning Path

### 1. **Basic Commands**
   - Start Claude Code: `claude`
   - Get help: `/help`
   - View MCP servers: `claude mcp list`

### 2. **Project Setup**
   - Create `CLAUDE.md` in your project root for project-specific instructions
   - Configure settings in `.claude/settings.local.json`

### 3. **Working with Code**
   - Ask Claude to read and explain code
   - Request code modifications and improvements
   - Generate tests and documentation

### 4. **Advanced Features**
   - Custom slash commands
   - Hooks configuration
   - Integration with MCP servers

## Resources

- **Official Documentation**: [Claude Code Docs](https://docs.claude.com/en/docs/claude-code)
- **MCP Protocol**: [Model Context Protocol](https://modelcontextprotocol.io/)
- **Serena MCP**: [GitHub Repository](https://github.com/oraios/serena)
- **Community**: [GitHub Issues](https://github.com/anthropics/claude-code/issues)

## Contributing

This is a learning repository. Feel free to:
- Add your own examples and learnings
- Share useful MCP server configurations
- Document workflows that worked well for you

## License

MIT

---

**Happy Learning!** 🚀
