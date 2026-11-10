---
title: Platform MCP Server
description: Connect MCP-compatible assistants and automation tools to Sherweb Cumulus.
---

## Overview

The Sherweb Cumulus MCP Server connects MCP-compatible assistants and automation tools to Cumulus through the Model Context Protocol (MCP). It exposes tools, prompts, and resources for working with Cumulus data through natural-language requests.

Available tools and actions depend on the permissions of the authenticated user or client account.

## What you can do

Depending on your account permissions, the server can help you work with:

* Organizations and subscriptions
* Product catalog and pricing
* Billing and charges
* Audit history and subscription changes
* Schema information

For example, you can ask: "Which subscriptions are expiring within the next 30 days?" Start with read-only requests and verify important results in Cumulus.

## Connect

See [Get started](docs/getstarted.md) for credential prerequisites, host-specific configuration, and authentication steps. Hosts differ in their setup and OAuth support; consult your host's current MCP documentation. The guide includes examples for VS Code, Cursor, and Microsoft Copilot Studio.

## Authentication and permissions

Authentication uses OpenID Connect with either authorization code with PKCE for interactive sign-in or client credentials for machine-to-machine workflows. See the [protected-resource metadata](https://mcp.sherweb.ai/.well-known/oauth-protected-resource/) for details.

The server performs backend operations on behalf of the authenticated user or client, using that identity's permissions. Tool visibility in a host does not necessarily mean your account is authorized to run that tool.

## Consent and safe use

Consent helps preserve human oversight:

* Read-only tool consent is requested once per session.

Review the requested action and its target before approving it. If an action's outcome is unclear, check its final state in Cumulus before trying again. Never share your Client Secret or access tokens.

## Support

* [Get started](docs/getstarted.md) to connect a host.
* [Troubleshooting](docs/troubleshoot.md) for common connection or usage issues.
* [Sherweb setup article](https://helpdesk.sherweb.com/en-us/knowledge-base/articles/KA-05021) for Cumulus-specific setup details.

For additional help, use your normal Sherweb support channel. Verify important results and changes in Cumulus.
