# System MCP Catalog

This repository contains catalog entries for system MCP servers.

## Contents

- Root-level `*.yaml` files define catalog entries.
- `.github/workflows/` contains the same automation used in the existing catalog repository.
- `scripts/` contains helpers for tool preview refresh, validation, and linting.
- `mcp-server-validation-automation/` contains the UI automation suite used by the workflows.

## Current Catalog Entries

- `pii-filter.yaml`: Catalog entry for `ghcr.io/obot-platform/pii-filter:v0.1.0`

## Repository Conventions

- Keep catalog entries as top-level YAML files.
- Use `containerizedConfig` for container-based MCP servers.
- Add `toolPreview` when the server tool surface is known.
- Keep workflow and validation support files aligned with the reference `mcp-catalog` repository.

## Automation

The repository includes the same workflow and support structure as the existing catalog repo, including:

- image tag update automation
- tool preview refresh
- validation automation
- vulnerability and MCPWN scanning workflows
- UI test automation support

Some workflows require GitHub Actions secrets such as `OPENAI_API_KEY` and access to GitHub Container Registry.
