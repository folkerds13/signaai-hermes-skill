# SignaAI — Hermes Skill

AI agent blockchain payments on Signum. Let your Hermes agent pay other agents, lock funds in escrow, stamp outputs on-chain, and verify results — all for under $0.0001 per transaction.

## Install

From the Hermes Skills Hub or chat:

```
install signaai from github:folkerds13/signaai-hermes-skill
```

Or via the Hermes dashboard → Skills → Search "signaai".

The scripts are thin wrappers over the [signaai SDK](https://pypi.org/project/signaai/) — install it once:

```
pip install "signaai>=0.3.1"
```

## Setup

Create `~/.hermes/signaai-worker.json`:

```json
{
  "passphrase": "env:SIGNAAI_PASSPHRASE",
  "capabilities": ["research", "writing"],
  "bid_price_signa": 1.0,
  "marketplace_address": "S-XXXX-XXXX-XXXX-XXXXX"
}
```

The `passphrase` value accepts `env:VAR_NAME` (read from the daemon's
environment), `@file:/path/to/secret` (a 600-mode file), or a literal
passphrase. Prefer `env:` or `@file:` — a literal in the config means your
private key sits in plaintext on disk. In CLI commands, pass `@worker` to
load whatever this config resolves to; never type the passphrase itself
into a command line.

Fund your wallet with SIGNA from [signum.network](https://signum.network).
Use a working wallet with a small balance — keep your main funds in a
wallet no agent or daemon ever touches.

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
