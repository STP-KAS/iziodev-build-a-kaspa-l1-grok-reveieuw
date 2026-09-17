# Sources

What each URL backs. Dates are when the source was published or when this desk read it. Recheck live endpoints before quoting as current.

## Primary: the thread and the person

| Source | What it backs |
| --- | --- |
| [x.com/IzioDev/status/2100178860700512752](https://x.com/IzioDev/status/2100178860700512752) | The onboarding claim. Three-post thread, 16 Sep 2026. |
| [THREAD.md](THREAD.md) | Full quote + resolved t.co targets. |
| [github.com/IzioDev](https://github.com/IzioDev) | GitHub login invited as collaborator. Romain Billot. |
| [x.com/IzioDev/status/2000490683598004383](https://x.com/IzioDev/status/2000490683598004383) | KEF grant, 15 Dec 2025. Mission = Kaspa Core. |
| [x.com/Kaspa_KEF/status/2000509077819171064](https://x.com/Kaspa_KEF/status/2000509077819171064) | KEF welcome: 15+ years, Kasia, Rusty Kaspa, PR 740 / VSPCv2. |

## Argent / Silverscript / template

| Source | What it backs |
| --- | --- |
| [github.com/argent-lang/argent](https://github.com/argent-lang/argent) README | Actor compiler. **Not release-ready.** Needs audit/hardening. Compiles `.ag` → Silverscript + artifact. |
| [github.com/argent-lang/argent-template](https://github.com/argent-lang/argent-template) README | Quick start. Scope: local runtime only. No network, no wallet, no submit. `./setup` clones current master. Windows: `setup.cmd`, `setup-win.ps1`. |
| [github.com/argent-lang/argent-playground](https://github.com/argent-lang/argent-playground) | End-to-end local demos. PR target named in the tweet. |
| [playground/ag](https://github.com/argent-lang/argent-playground/tree/master/ag) | Tweet example link 1 (resolved from t.co/AOcj7Kt7s7). |
| [argent/examples](https://github.com/argent-lang/argent/tree/master/examples) | Tweet example link 2 (resolved from t.co/PClgCOmueh). |
| [youtube.com/watch?v=xZsuvcc9qPk](https://www.youtube.com/watch?v=xZsuvcc9qPk) | Argent Live Coding #1: A Multi-Actor Ticketing App. |
| [github.com/argent-lang/argent-playground/pull/6](https://github.com/argent-lang/argent-playground/pull/6) | Izio name-service PoC. |
| [github.com/kaspanet/silverscript](https://github.com/kaspanet/silverscript) / [v1.0.0](https://github.com/kaspanet/silverscript/releases/tag/v1.0.0) | Foundation compiler. Stable release 9 Sep 2026. Does not certify Argent. |
| kaspaexplained [build-on-kaspa](https://kaspaexplained.com/build-on-kaspa) (read 17 Sep 2026; page baseline 14 Sep) | Three repos, zero releases. Argent ICC = unaudited offline demos. "One state, many writers: nothing public." |
| kaspaexplained [status](https://kaspaexplained.com/status) (checked 14 Sep 2026) | Native DeFi = Roadmap. "Argent proves production-ready" = does not hold. KCC-1/2/20 = Draft. |
| [docs.kaspa.org/toccata/argent](https://docs.kaspa.org/toccata/argent) | Cited via kaspaexplained: "design direction and prototype, not a production-stable API." |

## Protocol

| Source | What it backs |
| --- | --- |
| [rusty-kaspa v2.0.0](https://github.com/kaspanet/rusty-kaspa/releases/tag/v2.0.0) | Toccata activation DAA 474,165,565. |
| [cryptonews.net Toccata piece](https://cryptonews.net/news/altcoins/33429525/) (11 Sep 2026) | Activation ~16:15 UTC 30 Jun 2026. Covenants, OpZkPrecompile, tx v1. Distinct from Kasplex zkEVM. |
| [KIP-16](https://github.com/kaspanet/kips/blob/master/kip-0016.md), [17](https://github.com/kaspanet/kips/blob/master/kip-0017.md), [20](https://github.com/kaspanet/kips/blob/master/kip-0020.md), [21](https://github.com/kaspanet/kips/blob/master/kip-0021.md) | Active. ZK precompile, covenants/script, covenant IDs, sequencing commitment. |
| [kaspanet/kccs](https://github.com/kaspanet/kccs) | KCC-0/1/2/20 Draft. KCCs are not consensus. Izio co-author on 1, 2, 20. |
| [kaspanet/vprogs](https://github.com/kaspanet/vprogs) | Shared mutable state: roadmap / early development. |

## Stables and size of the L1 app layer

| Source | What it backs |
| --- | --- |
| [x.com/KaspaKaha/status/208314...](https://x.com/KaspaKaha) 31 Jul 2026 (quoted in-thread by others; text fetched) | Bridged stables Igra+Kasplex **$1.47M**: USDC $1.10M, USDT $370.7k. No native L1 issuer tracked. "When do we get proper stables on L1?" |
| [x.com/IzioDev/status/2092136862777253944](https://x.com/IzioDev/status/2092136862777253944) | "stablecoin implementation doesn't require vProgs. it can be done since 2 months on L1" |
| [x.com/IzioDev/status/2092296276763169135](https://x.com/IzioDev/status/2092296276763169135) | Established issuers landing = "illusion" for adoption. Juicy apps preferred. |
| [x.com/IzioDev/status/2092328445472538780](https://x.com/IzioDev/status/2092328445472538780) | Issuers "will naturally come" after apps grow. |
| [Kas-Smiths #143](https://kas-smiths.org/t/kusd-a-decentralized-oracle-free-kas-backed-stablecoin-on-l1/143) | KUSD: TN10, unaudited, KAS-backed, oracle-free via fixed module price. Not ready for real value. |
| [STP-KAS/kusdt-bitcoffee](https://github.com/STP-KAS/kusdt-bitcoffee) | Independent TN10 pass of KUSD. Not an audit. Peg unproven. No wallet pay path. |
| [kascov.io](https://kascov.io/) live JSON 17 Sep 2026 | Mainnet: 187,709 covenants ever, **811 active**, live_value **1,343,872 KAS**. Tip DAA 542036273. |
| [kascov templates](https://kascov.io/data/mainnet/templates.json) 17 Sep 2026 | `p2sh commitment` 1,342,318 KAS; **KCC20 token 1,530.71 KAS / 119 covenants**; SilverScript Escrow 4 covenants, 0 live. |
| [kascov price](https://kascov.io/data/price.json) 17 Sep 2026 | kaspulse signed **$0.033309**/KAS. Dollar figures in README use this print. |
| kaspaexplained developments (22 Aug 2026 snapshot, page later moved) | Then: ~1.75M KAS live covenants ≈ $51.2k at $0.02926. 109 KCC20 holding ~1,569 KAS. 86 token markets, 7 graduated AMMs. Lending absent. |
| [CoinEx cycle piece](https://www.coinex.com/en/insight/report/can-kas-survive-another-crypto-cycle-the-signals-that-matter-now-6a59d8102f8f1bbf5c08b91d) 17 Jul 2026 | Organic users + stablecoin liquidity named as survival signal. Kasplex weekly actives 169 (−97.8% from peak). KRC-20 selected names 97–99% off ATH. |
| [kaskad.app](https://kaskad.app/) | Lending is Igra L2, not Kaspa L1. USDC/USDT listed there. |

## Other context

| Source | What it backs |
| --- | --- |
| [x.com/IzioDev/status/2098034510138884580](https://x.com/IzioDev/status/2098034510138884580) | 10 Sep 2026: Toccata since 30 Jun; tooling still maturing; SilverScript/Argent/KCC confusion thread. |
| [github.com/IzioDev/kigs](https://github.com/IzioDev/kigs) | Earlier interactive getting-started (network/wallet/tx/UTXO/BlockDAG). |
| [docs.kaspa.org](https://docs.kaspa.org/) / [docs.kaspa.org/llms.txt](https://docs.kaspa.org/llms.txt) | Official docs. Izio previously pointed agents at llms.txt (30 Jun 2026). |

## What this desk did not use as proof

- Discord screenshots.
- Unverified "production use" claims in unmerged KCC PRs (KCC-21 / KCC-402).
- L2 TVL as evidence of an L1 dollar.
- Local `cargo run` success as evidence of a mainnet app.
