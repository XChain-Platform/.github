# XChain Platform

[XChain](https://xchain.io/) is an open token protocol for any blockchain,
live today on Bitcoin, Litecoin, and Dogecoin, with more chains coming. It
encodes a compact set of ACTIONs into ordinary on-chain transactions, then
indexes them into a deterministic, replayable ledger: tokens, transfers, a
built-in DEX, dispensers, smart contracts, cross-chain calls, and more, secured
by the host chains themselves rather than a new one. Adding a UTXO chain is a
configuration change, not a fork; account-based chains are on the roadmap.

- **Website:** [XChain Platform](https://xchain.io/)
- **Documentation:** [XChain Platform documentation](https://docs.xchain.io/)
- **Block explorer:** [XChain block explorer](https://explorer.xchain.io/)
- **Wallet:** [XChain Wallet](https://wallet.xchain.io/)

## How it fits together

```
Coin node (bitcoind / litecoind / dogecoind)
    -> utxo-tracker   (UTXO + balance queries)
    -> encoder        (builds the PSBT you sign and broadcast)
    -> coin node      (your transaction is mined)
    -> decoder        (reads blocks, decodes XChain ACTIONs)
    -> indexer        (applies ACTION logic, writes the ledger)
    -> explorer       (REST + JSON-RPC + web UI over the ledger)
       hub            (config oracle and cross-chain coordinator)
```

## Repositories

| Repo | What it does |
|---|---|
| [xchain-node](https://github.com/XChain-Platform/xchain-node) | One-command installer and manager for the whole stack |
| [xchain-encoder](https://github.com/XChain-Platform/xchain-encoder) | Builds unsigned PSBTs that embed XChain ACTIONs |
| [xchain-decoder](https://github.com/XChain-Platform/xchain-decoder) | Decodes XChain transactions from the chain into a database |
| [xchain-indexer](https://github.com/XChain-Platform/xchain-indexer) | Applies ACTION logic and writes the deterministic ledger |
| [xchain-explorer](https://github.com/XChain-Platform/xchain-explorer) | REST + JSON-RPC API and web block explorer |
| [xchain-hub](https://github.com/XChain-Platform/xchain-hub) | Config oracle, price feeds, and cross-chain coordination |
| [xchain-utxo-tracker](https://github.com/XChain-Platform/xchain-utxo-tracker) | Indexes UTXOs and serves balance queries |
| [xchain-sync](https://github.com/XChain-Platform/xchain-sync) | Replicates the ledger to validators |
| [xchain-vm](https://github.com/XChain-Platform/xchain-vm) | Deterministic smart-contract execution engine |
| [xchain-sdk](https://github.com/XChain-Platform/xchain-sdk) | Developer SDK for building XChain ACTIONs |
| [xchain-wallet](https://github.com/XChain-Platform/xchain-wallet) | Self-custodial multi-chain wallet (web, extension, desktop) |
| [xchain-contracts](https://github.com/XChain-Platform/xchain-contracts) | Smart-contract template library and scaffolding CLI |
| [xchain-documentation](https://github.com/XChain-Platform/xchain-documentation) | The protocol specification |

## Start here

- **See what it is:** the [XChain Platform](https://xchain.io/) site.
- **Use the platform:** the [Getting Started](https://docs.xchain.io/getting-started/) guide.
- **Build on it:** the [Developer Guide](https://docs.xchain.io/developer-guide/) and the [API Reference](https://docs.xchain.io/developer-guide/API_Reference.html).
- **Run a node:** [xchain-node](https://github.com/XChain-Platform/xchain-node).

## Security

Found a vulnerability? Please do not open a public issue. Use GitHub Private
Vulnerability Reporting on the affected repository, or email
**security@dankest.llc**. Each repository carries its own `SECURITY.md` with
scope and response details.

## Contributing

Contributions are welcome. See the `CONTRIBUTING.md` in each repository. The
organization-wide Code of Conduct applies to every repo; the canonical Code of
Conduct and the `MAINTAINERS.md` ownership and escalation list live in the
[`xchain-documentation`](https://github.com/XChain-Platform/xchain-documentation)
repository.

## License

XChain Platform is dual-licensed: the GNU Affero General Public License v3.0
(AGPL-3.0-or-later) for everyone, and a commercial license for organizations
that need to keep modifications private. "XChain" is a trademark of Dankest, LLC.
