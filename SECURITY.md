# Security Policy

This is the organization-wide default security policy for the XChain Platform.
Most repositories ship their own `SECURITY.md` with specific scope and response
detail; that file takes precedence where it exists. This default applies to any
repository that does not.

The XChain Platform is a token protocol on Bitcoin, Litecoin, and Dogecoin.
Several components touch real funds and consensus state, so we take reports
seriously and respond fast.

If you've found a security issue, please **do not open a public issue or pull request**. Use the private channels below.

## How to report

### Preferred: GitHub Private Vulnerability Reporting

Open a draft advisory from the **Security** tab of the affected repository
(`Report a vulnerability`). The advisory is private until we publish it.

### Alternative: Email

Email **security@dankest.llc** with:

- A description of the issue and the threat it poses.
- Reproduction steps or a proof-of-concept.
- The affected repository, version or commit, and the network you tested against (mainnet / testnet / regtest).
- Any patches or mitigations you'd like considered.

For sensitive reports, encrypt to our PGP key (fingerprint published alongside
the first signed release artifact); until then the email channel is acceptable
for first contact and we will coordinate an encrypted exchange before you share
proof-of-concept details.

We do not currently offer a paid bug bounty. We do offer public credit in the
advisory and release notes, unless you prefer to remain anonymous.

## Response timeline

| Stage | Target |
|---|---|
| Initial acknowledgement | within 72 hours |
| Triage + severity assignment | within 7 days |
| Fix or mitigation | within 30 days for high/critical, 90 days for lower severities |
| Coordinated public disclosure | up to 90 days from initial report, or sooner once a fix has shipped |

If we cannot meet a timeline, we will tell you why and propose a new one.

## Scope

Each repository's own `SECURITY.md` defines its in-scope and out-of-scope
surface. In general, in scope: anything in our code that risks user funds,
corrupts or forges consensus state, exposes credentials, or enables denial of
service. Out of scope: the underlying coin nodes and third-party dependencies
(report those upstream, though we still want to hear about them), and an
operator's own deployment, network, and credential hygiene.

If you are unsure, send the report anyway and we will tell you whether it falls
in scope.

## What we ask

- Give us a reasonable window to fix before disclosing publicly. The 90-day ceiling is firm; earlier is fine once a fix has shipped and users are protected.
- Test against regtest or testnet where possible. Mainnet proofs-of-concept are accepted but should be the minimum needed.
- Do not access data, or attempt to access data, beyond what is needed to demonstrate the issue, and do not run availability-impacting scans against shared infrastructure.
