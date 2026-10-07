# revrule-csv-import

**Import a revenue CSV into RevRule as economic events. By Payload.**

> **Status: early preview.** The CLI source is not published yet: this repo
> contains no source tree and the package is not on npm, so there is nothing
> to install right now. Everything below is grounded in the repo description
> and the v1.0.0 release notes only.

## Intended usage

From the v1.0.0 release notes:

```bash
npx revrule-csv-import --graph GRAPH_ID --api-key KEY
```

- `--graph GRAPH_ID`: the RevRule graph the events belong to
- `--api-key KEY`: your RevRule API key

Once published, the CLI will post each row of a revenue CSV to
[RevRule by Payload](https://github.com/Payloadhq/payload-flow), the
programmable revenue rules engine, as an economic event, so your existing
revenue history starts flowing through your revenue rules.

## Intended scope

It imports data. It does not define revenue rules, change payouts, or move
money. That stays in RevRule.

## Beyond import

- **When money moves, decide who earns what:** RevRule by Payload is the
  programmable revenue rules engine this CLI feeds.
- **Revenue infrastructure at scale:** Veyline by Payload is the production
  layer for x402 + MCP: autonomous economic control for machine commerce.

Built by [Payload](https://payloadhq.github.io/).

## License

MIT. See [LICENSE](LICENSE).
