# Shopify Store Scraper — E-commerce Migration Leads — MCP Server

Find e-commerce sites ready to migrate to Shopify from your AI agent or MCP client. Give it a list of sites and it detects WooCommerce, Magento, BigCommerce and OpenCart stores, analyzes their performance issues, and scores each one's migration readiness — as clean structured records.

This repo is the MCP listing for the [Shopify Store Scraper — E-commerce Migration Leads](https://apify.com/magnova/shopify-actor) Actor by Magnova on Apify. The server is hosted by Apify at the pinned endpoint below — there is nothing to install or run from this repository; you just point your MCP client at the URL.

## Tools

The pinned connection loads a focused tool set:

- **magnova--Shopify-Actor** — Detect WooCommerce, Magento, BigCommerce and OpenCart stores and score their Shopify migration readiness. Returns structured records: platform, performance issues, migration-readiness score.
- **fetch-actor-details** — Fetch the Actor's full input schema, pricing, and documentation, so an agent can check parameters and cost before running it.
- **get-actor-run / get-dataset-items** — Run and storage helpers, loaded automatically, used to fetch the results a run produced.

## Connect

Pinned endpoint (Streamable HTTP):

```
https://mcp.apify.com?tools=fetch-actor-details,magnova/Shopify-Actor
```

On first connect, your client will ask you to sign in with your Apify account (OAuth). If your client cannot do OAuth, pass your Apify API token as an `Authorization: Bearer <YOUR_APIFY_TOKEN>` header instead.

### Cursor / VS Code / other Streamable HTTP clients

```json
{
  "mcpServers": {
    "shopify-actor": {
      "url": "https://mcp.apify.com?tools=fetch-actor-details,magnova/Shopify-Actor"
    }
  }
}
```

### Claude Desktop

Claude Desktop's config file only runs local commands, so use the `mcp-remote` bridge:

```json
{
  "mcpServers": {
    "shopify-actor": {
      "command": "npx",
      "args": [
        "-y",
        "mcp-remote",
        "https://mcp.apify.com?tools=fetch-actor-details,magnova/Shopify-Actor"
      ]
    }
  }
}
```

The same pinned URL also lives in this repo's `.mcp.json`, and `server.json` is the listing for the Official MCP Registry, published as `io.github.memeanalyst/shopify-actor-mcp`.

## Pricing

Pay per event, billed to your own Apify account: **$0.005 per item returned — $5 per 1,000 items**. No start fee, no subscription, and you are only charged for records actually delivered.

## Links

- Actor on Apify Store: https://apify.com/magnova/shopify-actor
- MCP endpoint: https://mcp.apify.com?tools=fetch-actor-details,magnova/Shopify-Actor

*Store records come from the public pages of the sites checked.*
