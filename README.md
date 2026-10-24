# Ukiyo

## 1. Agents paying with x402 or MPP, no account

Buy GPU blocks at `POST https://pay.u-kiyo.ai/api/machine/gpu-blocks` or jobs at `POST https://pay.u-kiyo.ai/api/machine/gpu-jobs`. Use any standard x402 v2 exact USDC client on Base, or an MPP client for Solana USDC or Tempo USDC.e. No signup or API key is required.

Read [pricing](https://pay.u-kiyo.ai/api/pricing), send the purchase details, current legal acceptance and a P-256 recovery public key, then retry the same URL and body with the standard payment header. Save the returned access token and retain the recovery private key. Read the [complete payment, recovery and Bazaar guide](https://docs.u-kiyo.ai/connect/machine-payments) before paying.

Cloudflare operators: raise the default $0.10 payment cap to cover the approved quote ($5 minimum); `maxPaymentValue: 5_000_000n` covers $5 USDC. Keep a cumulative budget. Live ghost/stall fallback replaces failed provider instances within the purchased specifications and budget, confirms destruction before replacement, and issues exactly-once service credit if provisioning fails. Anonymous cards and inference are unavailable.

## 2. Agents and developers using the API with an account

The existing API-key/account-balance flow is unchanged: CLI `ukiyo` 0.2.5, local MCP `ukiyo-mcp` 0.2.0 and pinned Skill `ukiyo-compute` 1.0.1. These are existing release downloads, not new npm releases. The account instructions below apply to this path. Skill 1.0.1's immutable artifact references CLI 0.2.2; keep the separately installed CLI 0.2.5. See the full guide for artifact links and checksums.


**Rent a GPU. In Seconds. On Telegram.** Pick a GPU, fund your balance once, pay only for what you use.

[Website](https://u-kiyo.ai) · [Docs](https://docs.u-kiyo.ai) · [Live GPU prices](https://u-kiyo.ai/gpu/) · [Telegram](https://t.me/UkiyoComputeBot)

## Tools

| | |
| --- | --- |
| **[ukiyo-cli](https://github.com/ukiyocompute/ukiyo-cli)** | Command-line tool: sign up, add credit, rent, run commands, terminate |
| **[ukiyo-mcp](https://github.com/ukiyocompute/ukiyo-mcp)** | MCP server so AI agents in Cursor, VS Code and other clients can rent GPUs |
| **[ukiyo-skill](https://github.com/ukiyocompute/ukiyo-skill)** | Agent skill that teaches the full rental workflow |
| **[ukiyo-api](https://github.com/ukiyocompute/ukiyo-api)** | HTTP API, OpenAPI spec and examples |
| **[ukiyo-guides](https://github.com/ukiyocompute/ukiyo-guides)** | Step-by-step guides |

For AI agents: [llms.txt](https://u-kiyo.ai/llms.txt) · [llms-full.txt](https://u-kiyo.ai/llms-full.txt)

Contact: **contact@u-kiyo.ai**
