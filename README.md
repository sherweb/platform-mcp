# Platform MCP Server

## Overview

This is the MCP server exposing Cumulus MCP tools, prompts (templates) and resources, leveraging Sherweb internal APIs.

## Usage

Connect to the MCP server URI at <https://mcp.sherweb.com> for streamable HTTP transport. Tools can then be discovered by the agent when prompting in natural language. Prompt templates can also be used with slash commands. Follow the steps in this [knowledge base article](https://helpdesk.sherweb.com/en-us/knowledge-base/articles/KA-05021) for a successful journey.

### Authentication

The authentication uses OpenID Connect with either the authorization code with PKCE flow or the client credentials flow. See the [protected resource document](https://mcp.sherweb.com/.well-known/oauth-protected-resource/) for details.

> [!CAUTION]
> It is important to understand the MCP server performs requests in the backend on behalf of authenticated entity (user or client depending on the flow) and when operations are audited (usually non-readonly tool methods)

### Consent

Consent is a key principle of the MCP specification, so human oversight (aka human-in-the-loop or HITL) is maintained. Usually, managing consent is an MCP client responsibility, but it is implemented in this server also, with the following variants:

1. for read operations, the consent is asked once per session and scoped for all read-only tools
1. for update (write) operations, the consent is asked for every tool for every execution (this may seem to hinder the UX, but increases user control over the AI agent).
