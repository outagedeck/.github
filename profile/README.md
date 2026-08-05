# OutageDeck

**Is it you, or is it them?** Live status for 172 cloud and SaaS vendors, read from the official status feed each one publishes about itself, about every 10 minutes.

[![Live status for AWS, Cloudflare, GitHub, OpenAI, Vercel and Google Cloud | OutageDeck](https://outagedeck.com/embed/wall.svg?p=aws,cloudflare,github,openai,vercel,google-cloud)](https://outagedeck.com/stack?p=aws,cloudflare,github,openai,vercel,google-cloud)

That wall is not a screenshot. It is the same embed you can drop into your own README, rendering right now from those six vendors' own feeds. Click it for the full board.

## What you get

- **[Answer "is it us or them" in one click](https://outagedeck.com/stack)** with no account. Pick your vendors, or paste a `package.json` and let it match your dependencies in the browser. Nothing is uploaded, and the result is a shareable link.
- **[Free outage alerts](https://outagedeck.com/account)** on email for up to 5 providers, no card. Paid plans add Slack, Teams, Discord, and your own webhook, across your whole stack.
- **[A GitHub Action](https://github.com/outagedeck/status-check)** that checks AWS, Cloudflare, GitHub, OpenAI, and the rest of your vendor stack before a deployment proceeds. Add `uses: outagedeck/status-check@v1`; public checks are free and keyless.
- **[A cross-platform CLI](https://github.com/outagedeck/cli)** for status checks in a terminal or any CI system, with JSON output and configurable failure thresholds. Install it with Homebrew, Scoop, or `go install`.
- **[A TRMNL e-ink dashboard](https://github.com/outagedeck/trmnl-plugin)** for watching up to eight cloud and SaaS providers on one screen. It is free, keyless, and renders unavailable feeds as unknown instead of falsely healthy.
- **[A JSON API](https://outagedeck.com/developers/api)** with an [OpenAPI 3.1 spec](https://outagedeck.com/api/v1/openapi), open CORS, and anonymous access allowed.
- **[An MCP server](https://outagedeck.com/developers/mcp)** so a coding agent checks whether the cloud is down before it starts rewriting your code. Works in ChatGPT, Claude, Cursor, VS Code, and any MCP client, with no install and no key. Listed in the [official MCP registry](https://registry.modelcontextprotocol.io) as `com.outagedeck/outagedeck-status`; the prebuilt [Cloud and SaaS Outage Triage agent](https://awesome-copilot.github.com/agent/cloud-saas-outage-triage/) is published in GitHub Awesome Copilot with one-click installation.
- **[An installable Codex and Claude Code plugin](https://github.com/outagedeck/codex-plugins)** that bundles the MCP server with a dependency-outage triage skill. Add the public marketplace with `codex plugin marketplace add outagedeck/codex-plugins` or `claude plugin marketplace add outagedeck/codex-plugins`; both clients install version 0.1.1 successfully, and the package is validated against the live 14-tool MCP contract. The portable skill is also [listed with a passing security audit on skills.sh](https://www.skills.sh/outagedeck/codex-plugins/triage-dependency-outages).
- **[A dependency-free OpenClaw outage-triage skill](https://github.com/outagedeck/triage-dependency-outages)** that checks public vendor evidence before an agent changes code. Install the pinned release with `openclaw skills install git:outagedeck/triage-dependency-outages@v0.1.0`; it needs no OutageDeck account, API key, executable, or environment variable.
- **[Kubernetes workload dependency checks](https://github.com/outagedeck/kubectl-outagedeck)** through `kubectl outagedeck`, with explicit provider checks or read-only discovery from Deployment, StatefulSet, and DaemonSet annotations. Krew-validated releases cover macOS, Linux, and Windows.
- **[Prometheus and Grafana monitoring](https://github.com/outagedeck/prometheus-exporter)** with a production exporter, six-alert monitoring mixin, and nine-panel dashboard; plus ready integrations for [Home Assistant](https://github.com/outagedeck/home-assistant) and [Zabbix](https://github.com/outagedeck/zabbix-template).
- **[Independent uptime history](https://outagedeck.com/providers)** computed from what vendors actually published, kept linkable after the banner comes down.
- **[RSS feeds](https://outagedeck.com/feeds/incidents.xml)**, global and per provider.

## Put a live status wall in your README

Pick your vendors on the [embed builder](https://outagedeck.com/embed) and copy the snippet. It is an image inside a link, so it works in a README where iframes and scripts are stripped.

```markdown
[![Live status for your stack | OutageDeck](https://outagedeck.com/embed/wall.svg?p=aws,cloudflare,github)](https://outagedeck.com/stack?p=aws,cloudflare,github)
```

Add `&theme=light` or `&theme=dark` to pin the theme. Without it the wall follows the reader's own.

## Or a single provider badge

[![Live status for AWS | OutageDeck](https://outagedeck.com/api/v1/badges/aws)](https://outagedeck.com/providers/aws) [![Live status for GitHub | OutageDeck](https://outagedeck.com/api/v1/badges/github)](https://outagedeck.com/providers/github) [![Live status for Cloudflare | OutageDeck](https://outagedeck.com/api/v1/badges/cloudflare)](https://outagedeck.com/providers/cloudflare) [![Live status for OpenAI | OutageDeck](https://outagedeck.com/api/v1/badges/openai)](https://outagedeck.com/providers/openai)

```markdown
[![Live status for AWS | OutageDeck](https://outagedeck.com/api/v1/badges/aws)](https://outagedeck.com/providers/aws)
```

Swap `aws` for any of the [172 tracked providers](https://outagedeck.com/providers). Badges are deliberately outside auth and rate limiting, so they can be hotlinked freely.

## What we do not claim

We read what vendors publish. We do not probe them, so **we are never earlier than a vendor's own status page**, and anyone who needs detection before the vendor admits it needs synthetic monitoring instead. That constraint is the point: nothing here is crowd-reported or guessed, so there are no false positives. The reasoning behind every number is on [our methodology page](https://outagedeck.com/methodology), and OutageDeck publishes [its own status](https://outagedeck.com/status) in the same vocabulary it uses for everyone else.

---

OutageDeck is an independent project and is not affiliated with any of the providers it tracks. Provider names and logos are trademarks of their respective owners.
