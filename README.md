# revrule-csv-import

**Import a revenue CSV into RevRule as economic events. By Payload.**

Zero-dependency Node.js CLI. Point it at a revenue CSV and it posts each row
to [RevRule by Payload](https://payloadhq.github.io/), the programmable
revenue rules engine, as an economic event, so your existing revenue history
starts flowing through your revenue rules immediately.

## Install

```bash
npx revrule-csv-import <file.csv> --graph GRAPH_ID --api-key KEY
```

No install needed: `npx` fetches it on demand. Or install globally:

```bash
npm install -g revrule-csv-import
```

## Usage

```bash
revrule-csv-import revenue.csv --graph GRAPH_ID --api-key KEY
```

- `revenue.csv`: the revenue file to import
- `--graph GRAPH_ID`: the RevRule graph the events belong to
- `--api-key KEY`: your RevRule API key (kept out of the repo; pass via
  environment variable if you prefer)

One event per row. The CLI reports how many events were accepted and flags
rows it couldn't parse, so nothing imports silently.

## What it doesn't do

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
