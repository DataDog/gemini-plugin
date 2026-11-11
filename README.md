# Datadog Gemini Plugin

Query your Datadog data directly from Gemini and Gemini Agent using natural language. Ask about logs, metrics, traces, dashboards, monitors, and more.

The plugin connects Gemini to the Datadog MCP server. It runs entirely in Gemini's cloud, so there is nothing to install or configure on your computer.

## What you need

- A [Datadog](https://www.datadoghq.com/) account on the **US1** site (`app.datadoghq.com`). Other Datadog sites are not supported yet.
- Access to Gemini or Gemini Agent with the Datadog plugin enabled for your organization.

## Getting started

1. Ask your Gemini administrator to enable the Datadog plugin, if it is not enabled already.
2. Ask Gemini a question about your Datadog data.
3. When Gemini asks you to connect Datadog, sign in with your Datadog account and approve access.

## Using the plugin

Once connected, just ask anything about your Datadog data:

```
Show me error logs for the "checkout" service from the last hour
```

```
What monitors are currently alerting?
```

```
Find traces for service "api-gateway" with latency > 500ms
```

```
List my dashboards
```

## Can't connect?

**Your Datadog account is not on US1?** The plugin only connects to the US1 site. If you sign in to Datadog at an address other than `app.datadoghq.com` (for example `app.datadoghq.eu` or `us5.datadoghq.com`), the plugin can't reach your data yet.

**Sign-in fails or your data is missing?** Make sure you signed in to the Datadog organization that holds the data. To switch organizations, disconnect Datadog in Gemini and sign in again.

## Good to know

- Authentication uses OAuth with your Datadog account. Gemini only sees what your Datadog user can access.
- The plugin enables the Datadog MCP server's `core` toolset.
- No Datadog credentials are sent to the AI model provider.

## Support

- [Datadog MCP Server Documentation](https://docs.datadoghq.com/mcp_server/)

## Legal

See the [LICENSE](LICENSE) and [NOTICE](NOTICE) files included with this plugin.

For details on how Datadog handles your data, see the [Datadog Privacy Policy](https://www.datadoghq.com/legal/privacy).
