---
title: Troubleshoot
description: Diagnose common connection and usage issues with the Sherweb Cumulus MCP Server.
---

# Troubleshoot

Use these checks for common connection, authentication, and response issues.

[Get started](getstarted.html) · [Back to the documentation home](index.html)

## Common issues

| Issue | What to check |
| --- | --- |
| Sign-in or authentication fails | Confirm the selected flow, Client ID, and host configuration. For interactive sign-in, make sure the exact redirect URI from the host is registered in **Cumulus > Security > APIs**. Never share your Client Secret or token. |
| Tools are not available | Confirm the server URL is `https://mcp.sherweb.com`, complete authentication, and verify your Cumulus account has the required permissions. Refresh or reconnect the host. |
| The answer is incomplete | Add an organization, product, status, or date range. For long lists, request a smaller result or the next page. |
| The answer appears inaccurate | Compare the result with Cumulus and try a more specific request. Contact Sherweb if the underlying data differs. |
| An action fails or has an uncertain result | Do not immediately retry. Check the final state in Cumulus first. Contact Sherweb if the action is unexpected or affected the wrong organization or subscription. |
| Your host is not listed | Check the host's current MCP documentation. Compatibility and OAuth setup can vary by application and version. |

## Before contacting support

Use your normal Sherweb support channel. Include:

- Your partner name and Cumulus account or tenant identifier
- The MCP host application and version
- The authentication flow you selected
- The exact prompt or workflow, expected result, and actual result
- The date and time of the issue, including your time zone
- The error message and a screenshot, if available
- Whether the request was read-only or attempted to make a change

Remove Client Secrets, passwords, access tokens, authorization headers, and other sensitive values from screenshots, logs, configuration files, and recordings before sharing diagnostics.

For initial setup steps, return to [Get started](getstarted.html). For detailed Cumulus setup screenshots, see the [Sherweb setup article](https://helpdesk.sherweb.com/en-us/knowledge-base/articles/KA-05021).