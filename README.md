> **Experimental only. Not a product.** There is no spendable L1 stable on Kaspa, and no credible alternative on the horizon. Until the unit of account and the sequencing path are settled, production dapps are not a useful allocation of time or capital.
>
> Do not use wallet integrations on this GitHub. STP remains a clown. [DISCLAIMER.md](DISCLAIMER.md)

# iziodev build a Kaspa L1/Grok reveieuw

Independent Grok pass of [@IzioDev](https://x.com/IzioDev)'s 16 Sep 2026 thread: *"you too want to build a Kaspa L1 app and are unsure where to start?"*

Source post: [x.com/IzioDev/status/2100178860700512752](https://x.com/IzioDev/status/2100178860700512752)

This is not Argent. This is not Kaspa core. This is not an audit. This is not a grant review. It is a public desk pass of a builder-onboarding claim against what the repos, the compiler README, mainnet indexers, and Izio's own prior posts actually say.

@IzioDev ([GitHub](https://github.com/IzioDev)) is invited as a collaborator. Challenge it in issues. Do not treat silence as agreement.

> Clone `argent-template`, run `./setup`, follow a video, PR a playground demo. That is a **local compiler loop**. Calling it "build a Kaspa L1 app" without saying the template never touches the network is marketing. The missing rail is still the dollar.

Re-checked 17 Sep 2026 against live `argent-lang/argent` `master` (HEAD `e76ee07`). General-production row does not flip. One Argent README clause is stale (Silverscript v1.0.0 already shipped). See the verdict table.

## Verdict

| Claim | Holds? |
| --- | --- |
| Git + Rust is enough to start the loop | **Mostly.** Template exists. Smoke demo exists. |
| This onboards you onto Kaspa L1 | **No.** README: does not connect to a Kaspa network, manage a wallet, or submit transactions. |
| Argent is ready for general production use | **No.** Compiler README, still on `master`: "not yet release-ready" and "further audit and hardening before general production use." GitHub [releases](https://api.github.com/repos/argent-lang/argent/releases) `[]`, [tags](https://api.github.com/repos/argent-lang/argent/tags) `[]`. Latest commit (14 Sep) still adding security rules. |
| Expert early use of generated `.sil` | **Narrow path the README itself allows** — not general production. Advanced users who can verify generated contracts against the intended app. Do not round this up. |
| Silverscript foundation is stable | **Yes, as a compiler.** [v1.0.0](https://github.com/kaspanet/silverscript/releases/tag/v1.0.0) shipped 9 Sep 2026. Argent pinned to that commit on 10 Sep ([#60](https://github.com/argent-lang/argent/commit/867b080b973f93d75c4b7ca8ce06950a963accbb)). That does not certify Argent or an app. |
| Argent README is current on Silverscript | **No. Stale clause.** It still says "Once Silverscript completes its audit and is released…" after v1.0.0 exists. The not-release-ready / before-general-production sentences were **not** withdrawn. |
| Docs exist for a builder landing cold | **No.** Tweet 3 is a request to *write* the docs. |
| Helping people build is useful | **Yes.** Empty funnel is real. First-click clone is real. |
| That is enough for dapps | **No.** Dapps hate volatility. Kaspa L1 still has no dollar rail. |

**Bottom line:** interesting onboarding. Premature as a product path. Argent is not general-production. The stables hole is not a side note. It is the blocker.

## The question that the thread does not ask

**Where is the L1 dollar?**

Dapps do not hate Kaspa. They hate a unit of account that moves 10% because a PoW coin had a week. Lending, DEX quotes, payroll, invoices, NFT floors, agent budgets, merchant checkout: they price in a stable, or they do not ship. This is not ideology. It is how every chain that actually got DeFi did it.

Izio's own line, 25 Aug 2026:

> "stablecoin implementation doesn't require vProgs. it can be done since 2 months on L1"
>
> [x.com/IzioDev/status/2092136862777253944](https://x.com/IzioDev/status/2092136862777253944)

Then the causal story he actually believes:

> "i believe it is an illusion that well-established stablecoin issuers building one of their antenna on Kaspa would bring significantly more Kaspa adoption somehow. but i'm almost certain that juicy apps would, and that's more interesting too"
>
> [x.com/IzioDev/status/2092296276763169135](https://x.com/IzioDev/status/2092296276763169135)
>
> "stable issuers will naturally come as the app ecosystem organically grows (juicy apps)"
>
> [x.com/IzioDev/status/2092328445472538780](https://x.com/IzioDev/status/2092328445472538780)

That order is backwards. Uniswap without USDC is a casino. Aave without a borrowable dollar is circular leverage on the native token. A "Kaspa L1 app" whose only asset is KAS is a volatility product wearing an app costume.

**Helping people compile counters is interesting. The lack of stables remains.** Do not confuse a compiler tutorial with an economy.

### What the rails actually look like (17 Sep 2026)

| Rail | Status | Scale |
| --- | --- | --- |
| Native L1 USD issuer (USDT/USDC-class) | **None tracked.** KaspaKaha, 31 Jul 2026. | Zero. |
| Bridged L2 stables (Igra + Kasplex) | Live on L2 only | **$1.47M** total on 31 Jul 2026: USDC $1.10M, USDT $370.7k. Most in lending. DEX pools tiny. |
| KUSD (BitCoffee0, SilverScript covenants) | TN10. Unaudited. KAS-overcollateralized. Oracle-free by using a **fixed** module price. | Not a dollar. Still KAS vol. Desk pass: [STP-KAS/kusdt-bitcoffee](https://github.com/STP-KAS/kusdt-bitcoffee). |
| KCC-20 on L1 | Draft convention, not a ratified standard | kascov mainnet 17 Sep 2026: **119** KCC20 covenants, **1,530.71 KAS** live (≈ **$51** at $0.0333). |
| Live L1 covenant value | Real, small | kascov: **1,343,872 KAS** in 811 active coins (≈ **$44.8k**). Almost all is unlabeled `p2sh commitment`, not apps. |
| SilverScript escrow on mainnet | Four covenants, all burned | Live value **0**. |
| Native L1 DeFi as a product layer | **Roadmap** ([kaspaexplained.com/status](https://kaspaexplained.com/status), 14 Sep 2026) | Lending absent on L1. Kaskad is Igra L2. |

kascov snapshot used here: `https://kascov.io/data/mainnet-live.json` at tip DAA **542036273**, `live_value` **134387246092616** sompi. Price: kaspulse signed $0.033309/KAS (`https://kascov.io/data/price.json`). Template split: `https://kascov.io/data/mainnet/templates.json`.

If the entire L1 token layer is fifty-one dollars, you do not have a dapp platform. You have a compiler and a hope.

Igra/Kasplex stables exist. They are not L1 rails. They are bridged EVM IOUs sitting in a handful of L2 pools while Kasplex weekly actives fell **97.8%** from peak (CoinEx, 17 Jul 2026). That is not a substitute for a Kaspa-native unit of account.

**Firm:** a KEF core grantee can say "just build juicy apps" because his job is the compiler and the conventions. A product team cannot. Volatility is the product. Until there is a spendable L1 dollar — issuer-backed, or a collateralized design that actually holds a peg against a real DEX — onboarding more Rust programmers produces more local `cargo run` demos. It does not produce dapps.

## What Izio did

The thread is three posts.

**Post 1 — hook.** "you too want to build a Kaspa L1 app and are unsure where to start?"

**Post 2 — the loop.**

1. Install Git and Rust. "the only requirements as of today."
2. `git clone https://github.com/argent-lang/argent-template`
3. `./setup`
4. Follow [Argent Live Coding #1: A Multi-Actor Ticketing App](https://www.youtube.com/watch?v=xZsuvcc9qPk)
5. Look at [argent-playground/ag](https://github.com/argent-lang/argent-playground/tree/master/ag) and [argent/examples](https://github.com/argent-lang/argent/tree/master/examples)
6. PR your app to `argent-lang/argent-playground`
7. Ask in Kaspa Discord `development`

**Post 3 — docs that do not exist yet.** He asks the community to shape the next documentation site:

- Argent: Getting Started
- Specialized cookbooks
- Concept section

Acceptance criteria he posted, and they are the right ones:

- no unnecessary jargon; required terms go in Concept
- human-friendly (which also happens to be LLM-friendly)
- mermaid diagrams, no padding
- docs should not describe Argent or how it operates; they should describe **how to use it**
- existing programmability docs will likely be thrown away

Quoted thread: [THREAD.md](THREAD.md).

Surrounding work, not in the thread, that is still his:

- KEF grantee since 15 Dec 2025, mission stated as Kaspa Core ([grant post](https://x.com/IzioDev/status/2000490683598004383)).
- Co-author of [KCC-1](https://github.com/kaspanet/kccs/blob/main/kcc-0001.md) (covenant ABI) and [KCC-2](https://github.com/kaspanet/kccs/blob/main/kcc-0002.md) (authority schemes); co-author on [KCC-20](https://github.com/kaspanet/kccs/blob/main/kcc-0020.md) (fungible token). All **Draft**.
- First Argent app: name-service PoC, [argent-playground PR #6](https://github.com/argent-lang/argent-playground/pull/6).
- Co-author on Argent security work still landing on `master` (e.g. [leader/delegator rules 5 and 6](https://github.com/argent-lang/argent/commit/e76ee07f8b2719e8c06eee085ca3d613cc2b56e7), 14 Sep 2026). That is pre-release compiler work, not a production stamp.
- Earlier builder-hub / starter-kit work (`npx @kluster/kaspa-starter-cli`, KIGS).

## Why he did it

The honest reasons, not the marketing ones:

1. **Toccata is live and the funnel is empty.** Covenants activated 30 Jun 2026 at DAA 474,165,565. Ten weeks later a core grantee still has to post "where to start." That is a signal.
2. **The stack names collide.** SilverScript vs Argent vs KCC vs KRC-20 vs vProgs. He asked on 10 Sep 2026 if confusion remained. It does. A three-step clone is cheaper than another architecture thread.
3. **His job is Core, not DeFi.** KEF mandate is protocol. Compiler onboarding is in-scope. A Circle integration is not. That is why the thread never mentions a dollar.
4. **Argent is Sutton's compiler with almost no writers.** Three repos, no releases, single-digit/low-20s stars as of mid-September. Playground PRs are how you get a second author.
5. **Docs last is a pattern, not an accident.** Ship the language, then ask the internet to write Getting Started. Fast for the compiler. Hostile for the builder who believed tweet 1.

None of that is malice. It is a core-dev local optimum. The local optimum is not the ecosystem's.

## What Grok did

1. Fetched the full thread, replies, and Izio's Aug 2025–Sep 2026 stables posts.
2. Read `argent-lang/argent` README (status + "not release-ready"), `argent-template` README (scope: local runtime only), `argent-playground` layout.
3. Read [kaspanet/kccs](https://github.com/kaspanet/kccs) index: KCC-0/1/2/20 all Draft. Izio is on 1, 2, and 20.
4. Read [kaspaexplained.com/build-on-kaspa](https://kaspaexplained.com/build-on-kaspa) and [status](https://kaspaexplained.com/status) (checked 14 Sep 2026): Argent ICC = unaudited offline demos; native DeFi = Roadmap; "Argent proves production-ready contracts" = Research / does not hold.
5. Pulled live kascov mainnet stats and template breakdown (17 Sep 2026).
6. Cross-checked L2 stables (KaspaKaha 31 Jul 2026), Kasplex/Igra retention (CoinEx 17 Jul 2026), KUSD TN10 (Kas-Smiths #143 + [STP-KAS/kusdt-bitcoffee](https://github.com/STP-KAS/kusdt-bitcoffee)).
7. Did **not** run `./setup` in this pass. Did **not** submit a covenant to mainnet or TN10 from the template. The template's own README makes that a different job.
8. **Re-check, 17 Sep 2026:** re-fetched Argent README, [releases](https://api.github.com/repos/argent-lang/argent/releases) `[]`, [tags](https://api.github.com/repos/argent-lang/argent/tags) `[]`, Silverscript v1.0.0, Argent pin commit `867b080` / PR #60, HEAD `e76ee07` (security rules 5–6, IzioDev co-author). Split the verdict: general production **No**; expert `.sil` path is the README's own narrower sentence. Stale "once Silverscript is released" clause noted. Production row does not flip.

This is a claim review, not a compiler audit.

## Resources the thread points at — and what they actually are

| Resource | What the tweet implies | What it is |
| --- | --- | --- |
| [argent-template](https://github.com/argent-lang/argent-template) | Start here, build an L1 app | Sibling checkout of `argent` + local `argent-runtime`. **No node. No wallet. No submit.** Counter app is disposable. |
| `./setup` | One command | Unix. Tweet says "terminal / powershell". Windows files exist (`setup.cmd`, `setup-win.ps1`) and were not named. Setup clones **current `master`**, not a pin. |
| [YouTube xZsuvcc9qPk](https://www.youtube.com/watch?v=xZsuvcc9qPk) | Follow this | Sutton live-coding a multi-actor ticketing app. Useful. Not a deploy guide. |
| [playground/ag](https://github.com/argent-lang/argent-playground/tree/master/ag) | Working examples | Client-side Rust demos: counter, signed counter, two-actor exchange, ICC, dex_asset. Same local runtime. |
| [argent/examples](https://github.com/argent-lang/argent/tree/master/examples) | Working examples | Compiler examples: tickets, spawns, stones, toy chess, ICC, open ICC. |
| PR to playground | Ship your app | Ship a **demo binary**. Not a mainnet program. |
| Discord `development` | Support | Real. Not a substitute for docs, versions, or a chain submit path. |

Official Argent status, quoted because people will round it up. Re-fetched from `master` 17 Sep 2026:

> The project is still under active development and is not yet release-ready. Once Silverscript completes its audit and is released, advanced users who can review the generated `.sil` contracts will have a viable path to careful early production use. … Argent itself will still need further audit and hardening before general production use.
>
> — [argent-lang/argent README](https://github.com/argent-lang/argent)

Split that paragraph. Do not weld it into one "ready" or one "useless."

- **Stale:** "Once Silverscript completes its audit and is released" — Silverscript [v1.0.0](https://github.com/kaspanet/silverscript/releases/tag/v1.0.0) shipped 9 Sep 2026. Argent targeted it on 10 Sep. The README was not updated.
- **Still live, still binding:** "not yet release-ready" and "before general production use." Zero releases. Zero tags. Security rules still landing.
- **Narrow, not general:** "advanced users who can review the generated `.sil`" is expert early use. It is not an onboarding claim for tweet 1.

Kaspa docs called Argent "a design direction and prototype, not a production-stable API" ([docs.kaspa.org/toccata/argent](https://docs.kaspa.org/toccata/argent), via kaspaexplained).

Also missing from the tweet, present in the stack:

- No `getUtxosByCovenantId` RPC. You cannot ask a node for "this app's coins." Indexers (kascov, simply-kaspa-indexer) are the workaround. The template does not mention this because it never talks to a node.
- KCC-20 is Draft. Wallets and indexers are not required to speak it.
- Shared mutable state (many users, one app state) is vProgs / roadmap. Argent ICC is atomic multi-app txs in **offline demos**.
- The playground DEX is a single pair in a local runtime. It is not a market.

## Improvements

Required, not nice-to-have. Ordered by how much the current thread misleads.

1. **Say the scope in tweet 2, not in a README footer.** One line: *this compiles and executes locally; it does not hit Kaspa.* If you will not say it on X, do not title the thread "build a Kaspa L1 app."
2. **Pin a compiler revision.** `setup` taking floating `master` is how a Getting Started from Tuesday fails on Thursday. Tag `argent` even if the tag says `preview`.
3. **Windows commands in the tweet that mentioned PowerShell.** `./setup` is not PowerShell. `setup.cmd` / `setup-win.ps1` exist. Use them.
4. **Docs before the invitation.** Crowdsourcing Getting Started *after* telling people to start is inverted. His own criteria are good. He should ship one page that meets them, then ask for cookbooks.
5. **A "what you cannot build yet" page.** No shared global state. No L1 dollar. No general-production Argent. No covenant-UTXO RPC. No audited ICC. Vaults/escrow/spend-caps: yes, on chain, in Silverscript. "DeFi app": no.
6. **A testnet submit path in the template.** Until `cargo run` produces an accepted TN10 txid, this is a language playground. kascov already deploys SilverScript Mecenas/Escrow/LastWill on TN10 from a browser. The official Argent template should not be strictly weaker than that.
7. **Stop the apps-first, stables-later story.** It is false as economics even if it is comfortable as core work. Either:
   - name a concrete L1 dollar path (issuer covenant, or KUSD-class with a real DEX and a wallet pay path), or
   - say plainly: *build vaults and tickets; do not build a DEX/lending/checkout until a dollar exists.*
8. **Do not round KCC Drafts up to standards.** He published them. They are Draft. Tweet-level onboarding that implies a token standard exists is how you get another KRC-20 graveyard with extra steps. KRC-20 already did the "tokens exist, liquidity does not" cycle: selected names **97–99%** off ATH by mid-July 2026 (CoinEx).
9. **One mainnet reference app with a txid.** Name service PoC, chess, dex_asset: show an *accepted* transaction, or stop calling them L1 apps in public.
10. **KEF / Discord: put the dollar on the core agenda as infrastructure, not as "someone else's juicy app."** A unit of account is rails. Rails are Core. Treat it that way or admit Core is choosing not to.
11. **Fix the Argent README Silverscript clause.** v1.0.0 shipped. Either withdraw "once Silverscript is released" or people will quote the paragraph as if the foundation never landed — or, worse, as if Argent landed with it.

## Conclusion

Izio did a competent first-click. Git, clone, setup, video, playground, PR, Discord. For a language that is still unreleased, that is more than most Kaspa surfaces have offered. Credit that. Do not inflate it.

He did **not** give people a way to build a Kaspa L1 app in the sense anyone outside the compiler room means it. The template does not talk to Kaspa. Argent is not release-ready for general production. A stale README sentence about Silverscript does not change that. The docs he wants are the docs he did not write. The token convention is Draft. The live L1 token layer is about fifty dollars. The live L1 covenant layer is about forty-five thousand dollars, mostly unlabeled P2SH. Bridged L2 stables are a million and a half, elsewhere, and shrinking in users.

**Dapps hate volatility.** Helping people build is fine. It is not an answer to the missing rail. "Juicy apps will attract stables" is the sentence you say when you do not want to do the dollar. The implementation has been possible on L1, by his own post, since roughly late June. It is still not there.

Until a spendable L1 stable exists — not a TN10 experiment, not an Igra IOU, not a KAS-backed toy with a frozen price — this thread onboards hobbyists into a sandbox. That can be worth doing. Call it that.

@IzioDev: you are invited. If the template now submits, if Argent is tagged, if a dollar path is in writing, open a PR and correct the table. Until then the verdict stands.

## Files

- [THREAD.md](THREAD.md) — quoted X thread
- [SOURCES.md](SOURCES.md) — every URL, with what it backs

## License

MIT. No warranty. Not financial advice. Not Kaspa core. Not an audit of Argent, Silverscript, or KEF.

---

> **Standard disclaimer.** This GitHub, not the topic above.
>
> Intentions are good; thought process is questionable. STP remains delusional. Si vis pacem, para bellum.
>
> Intern at https://sixpack.wtf/  
> X: https://x.com/StppStp · GitHub: https://github.com/STP-KAS
