# Skills this agent actually uses

This folder is the working skill set of the agent that built this guide.
Nothing here is a wish list: every skill named below is installed in this
agent's workspace and has been used on real work. The full list is
`SKILL-INDEX.md` — 85 skills in total (58 bundled, 27 custom). This file
says which ones matter for the work in this repo, what each one is for, and
when to load it.

Read a skill's `SKILL.md` before you use it. A name alone is not the
instructions.

## The make.fun loop — load these first

- **makefun_bounty_preflight** — the preflight for every bounty: read the
  site skill, check the bounty requirements and the entry quota, check the
  kit version, and stop before building when `can_submit` is false. A
  broad direction to enter bounties is not a grant to spend money, so a
  bounty that needs paid credits or an entry fee still needs a yes first.
- **make.fun skill.md** (`https://make.fun/skill.md`) — the whole entry
  loop in eight steps: keypair and key, read the requirements, get the kit,
  build, bundle the transcripts, check, submit, claim. Fetch it again when
  the heartbeat shows a newer version.
- **documents**, **docx**, **pdf**, **xlsx** — reading and writing the
  deliverables themselves: reports, spreadsheets, decks, PDFs. Keep the
  editable source beside anything you export.

## Bug bounties — find it, prove it, report it

- **agentic-bug-hunter** — the hunt toolkit: recon, then hunt, then
  validate, then report, for HackerOne, Bugcrowd, Intigriti and Immunefi.
  Scope first, always. No theoretical bugs: a finding counts only when a
  proof of concept runs.
- **bug_bounty_hunt_discipline** — the discipline around the hunt: the
  7-Question Gate, one report per bug, severity from the CVSS score without
  inflating it, and the rule that an empty round is filed silently.
- **bsc-contract-audit** — evidence-based due diligence on BNB Smart Chain
  token contracts, NFT mints and deposit-refund "lock" mechanics. Read the
  contract before believing the post about it.
- **launch-curve-audit** — audit a token launch curve on BSC: bonding
  curve or tranche IEO, Agent-ID or allowlist gating, and where the money
  actually goes.
- **graphify** — turn a codebase into a knowledge graph for bug-hunt
  recon: file relationships and architecture, before you start reading
  code line by line.

## On-chain work — the safety rails are always on

- **onchain-safety-rails** — always on, for any signing, broadcast,
  approval, swap, bridge or stake: never touch or log seed phrases,
  private keys or keystore material; act only on wallets the owner named;
  simulate before broadcast; confirm before signing, with a one-line
  summary (chain, from, to, asset, amount, spender, fee); exact-amount
  approvals by default, unlimited only on an explicit extra yes; fail
  closed on ambiguity.
- **bsc_mint_preflight** — funding and gas preflight before any BSC
  fair-launch mint or claim through the Binance agentic wallet, so a
  top-up to the wrong wallet or a stale gas guess never costs an
  allocation.
- **explorer_first_balance_check** — verify a wallet balance or network on
  the chain explorer before stating it, so a stale wallet display never
  turns into a false alarm.
- **binance-agentic-wallet** — the Binance agentic wallet: pairing,
  status, and contract calls through the `baw` CLI. The session is the
  source of truth, not the app screen, and only the owner can re-pair.
- **fastmint** — fast first-come-first-served minting on BSC through the
  agentic wallet: preview, then one broadcast only, with the safety rails
  (free means value 0, paid needs an explicit amount and a cap).
- **free-mint-hunter** — discover free NFT mint opportunities and verify
  the project's social presence before acting on a "FREE Mint" post.
  Several of those posts turned out to be paid lanes, so verify on-chain.

## Telegram mini-apps and wallet identification

- **telegram_mini_app_claims** — claim daily rewards in Telegram
  mini-apps through Telegram Web and report balances that reconcile.
  Scope is the free claim only: never buy, upgrade, or stake.
- **wallet_app_identification** — identify which wallet app holds an
  address by the address the app displays, so an address alone never
  turns into the wrong app.

## Building and shipping software

- **frontend-design** — distinctive, intentional visual design when
  building new UI or reshaping an existing one.
- **webapp-testing** — test a local web application with Playwright:
  functional checks, and the same flows a user would run.
- **web-artifacts-builder** — build elaborate multi-component HTML
  artifacts (pages and apps the owner keeps and revisits).
- **animation-video-toolkit** — animation and video work: making videos,
  animating illustrations, 3D scenes, particles.
- **agent-browser** and **agent-browser-dogfood** — drive a real browser
  (snapshot-and-ref workflow), and systematically explore a web app to
  find bugs and UX issues. Always with an allowlist of domains on
  untrusted pages, and never a seed phrase in the auth vault.
- **mcp-builder** — build MCP servers so a model can talk to a service
  through a typed interface.
- **skill-creator** — create a new skill, improve an existing one, and
  measure whether it works.
- **custom-connector-setup** — connect a service this agent does not
  bundle, through its API or MCP server, and keep the credential in the
  secure connection flow.

## Research and communication

- **grok_x_search** — search public X posts, reactions and threads
  through the Grok Build CLI's `x_search`, for what people are saying
  about a topic.
- **image-search** — search the web by text for image URLs and source
  pages, for feeds, artifacts and visual references.
- **wide-research** — research across many sources before answering a
  question that needs breadth.
- **translation** — translate text between languages.
- **messaging** and **email-management** — message people from the
  owner's own accounts, and find, triage, draft and send email from the
  right mailbox.
- **social-publishing** and **social-content-performance** — publish to
  social accounts and read how the posts performed.
- **media-library** — search and inspect the owner's photo library.
- **transcribe-recordings** and **spoken-audio** — transcribe audio or
  video, and send a voice note or narrated summary.

## Everything else

The remaining skills (flights, hotels, shopping, groceries, health,
scheduling, music, and the rest) are loaded only when the owner asks for
that kind of work. They are listed in `SKILL-INDEX.md`. A skill is never
loaded "just in case".

## Known gaps — stated plainly

- There is no dedicated 3D or game-engine skill here (no Three.js,
  Godot, Blender or Unity playbook). Game bounties are built with the web
  skills above — frontend design, web app testing, artifacts — and that
  is a thinner bench than a game-focused kit.
- There is no dedicated web2 vulnerability-class skill (no separate
  XSS / SQLi / SSRF / JWT / GraphQL playbook). Web2 hunting runs through
  `agentic-bug-hunter`'s methodology plus the recon tools, and findings
  are validated with a proof of concept, never asserted from a pattern.
- The count is 85, not hundreds. A bigger number would be padding: these
  are the skills installed and used, and the index names every one of
  them so the claim can be checked.
