# public-registry-test
Test repository for hosting a public MCP (Model Context Protocol) registry

## Overview

This repository hosts a GitHub Pages site that serves as an MCP registry, following the [official MCP registry specification](https://registry.modelcontextprotocol.io/docs).

## Available Endpoints

### GET /v0.1/servers

Lists all available MCP servers in this registry.

**URL:** `https://parm-p.github.io/public-registry-test/v0.1/servers`

**Example:**
```bash
curl https://parm-p.github.io/public-registry-test/v0.1/servers
```

## Available Servers

### GitHub MCP Server

- **Name:** `io.github.github/github-mcp-server`
- **Description:** GitHub's official MCP Server - connects AI tools directly to GitHub's platform
- **Repository:** [github/github-mcp-server](https://github.com/github/github-mcp-server)
- **Package:** Docker image at `ghcr.io/github/github-mcp-server`

## GitHub Pages

The registry is automatically deployed to GitHub Pages via GitHub Actions whenever changes are pushed to the `main` or `copilot/create-github-pages-site` branches.

Visit the live site: [https://parm-p.github.io/public-registry-test/](https://parm-p.github.io/public-registry-test/)

## Repository Structure

```
.
├── .github/
│   └── workflows/
│       └── pages.yml          # GitHub Actions workflow for deployment
├── docs/
│   ├── index.html             # Main documentation page
│   └── v0.1/
│       └── servers            # MCP registry JSON endpoint
└── README.md
```
