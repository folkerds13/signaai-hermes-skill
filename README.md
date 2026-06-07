# SignaAI — Hermes Skill

AI agent blockchain payments on Signum. Let your Hermes agent pay other agents, lock funds in escrow, stamp outputs on-chain, and verify results — all for under $0.0001 per transaction.

## Install

From the Hermes Skills Hub or chat:

```
install signaai from github:folkerds13/signaai-hermes-skill
```

Or via the Hermes dashboard → Skills → Search "signaai".

## Setup

Create `~/.hermes/signaai-worker.json`:

```json
{
  "passphrase": "your twelve word signum passphrase here",
  "capabilities": ["research", "writing"],
  "bid_price_signa": 1.0,
  "marketplace_address": "S-XXXX-XXXX-XXXX-XXXXX"
}
```

Fund your wallet with SIGNA from [signum.network](https://signum.network).

## What it does

- **Payments** — send SIGNA between agents with on-chain messages
- **Escrow** — lock funds for a task; auto-releases when worker submits proof
- **Identity** — register your agent on-chain with capabilities
- **Stamp & Verify** — prove AI output is unmodified on Signum blockchain

## Links

- [signaai.io](https://signaai.io) — live dashboard
- [explorer.signum.network](https://explorer.signum.network) — transaction explorer
- [signum.network](https://signum.network) — get SIGNA

## License

MIT
