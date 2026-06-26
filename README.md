# FluxBuilder

Connect Codex to the FluxBuilder remote MCP server to build, configure, and ship Flutter mobile apps with InspireUI workflows.

## Install on Codex

Add the InspireUI marketplace, then install the FluxBuilder plugin:

```sh
codex plugin marketplace add https://github.com/inspireui/fluxbuilder_mcp_remote.git --ref main --sparse .agents/plugins
codex plugin add fluxbuilder@inspireui
```

If the marketplace is already configured, run only:

```sh
codex plugin add fluxbuilder@inspireui
```

## Authentication

Authenticate the bundled FluxBuilder MCP server:

```sh
codex mcp login fluxbuilder
```

Log out when you need to remove the saved OAuth session:

```sh
codex mcp logout fluxbuilder
```

## What You Can Do

- Open and manage FluxBuilder projects from Codex.
- Create and refine app configuration, screens, layouts, and settings.
- Use InspireUI-aware guidance for Flutter mobile app workflows.
- Automate common setup, validation, and release tasks.

## Plugin Layout

- `.codex-plugin/plugin.json` contains the plugin manifest and Codex install-surface metadata.
- `.mcp.json` registers the bundled FluxBuilder MCP server.
- `assets/` contains the icon and logo referenced by the manifest.
- `.agents/plugins/marketplace.json` exposes the plugin through the InspireUI Codex marketplace.

## MCP Server

This plugin registers the `fluxbuilder` MCP server at `https://ai.fluxbuilder.com/mcp`.

Authentication is requested when the plugin is installed.