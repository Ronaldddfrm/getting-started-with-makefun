# Skill index — all 85 skills

Every skill installed in this agent's workspace, grouped by where it is
used. 58 bundled skills plus 27 custom skills: 85 in total. The one-line
note after each name is what the skill is for, taken from the skill itself.
`fastmint.bak-20261111` is a backup of an older fastmint version and is not
counted as a skill.

## Custom skills (27) — built for this owner's real work

### Earn: make.fun and bug bounties

- **makefun_bounty_preflight** — preflight for a make.fun bounty:
  requirements, quota, kit version; stop before building when
  `can_submit` is false.
- **agentic-bug-hunter** — bug-bounty toolkit: recon, hunt, validate,
  report (HackerOne, Bugcrowd, Intigriti, Immunefi). Scope-first, no
  theoretical bugs.
- **bug_bounty_hunt_discipline** — hunt discipline: the 7-Question Gate,
  one report per bug, honest severity.
- **bsc-contract-audit** — due-diligence audit for BSC token contracts,
  NFT mints and deposit-refund locks.
- **launch-curve-audit** — audit a token launch curve on BSC
  (bonding curve, tranche IEO, allowlist gating).
- **graphify** — codebase to knowledge graph, for bug-hunt recon.

### Earn: on-chain mints and wallets

- **onchain-safety-rails** — always-on rails for any on-chain move:
  keys, user-funds-only, simulate-before-send, confirm-before-sign.
- **bsc_mint_preflight** — funding and gas preflight before a BSC
  fair-launch mint or claim.
- **explorer_first_balance_check** — verify a balance or network on the
  chain explorer before stating it.
- **binance-agentic-wallet** — Binance agentic wallet: pairing, status,
  contract calls via the `baw` CLI.
- **fastmint** — fast FCFS mint on BSC through the agentic wallet
  (broadcast target under 5 seconds).
- **free-mint-hunter** — discover free NFT mints and verify the project's
  X presence before acting.

### Earn: Telegram and wallets

- **telegram_mini_app_claims** — claim daily rewards in Telegram
  mini-apps and report balances that reconcile.
- **wallet_app_identification** — identify which wallet app holds an
  address by the address the app displays.

### Build and test

- **frontend-design** — distinctive, intentional visual design for new
  UI.
- **webapp-testing** — test local web apps with Playwright.
- **web-artifacts-builder** — build elaborate multi-component HTML
  artifacts (pages and apps).
- **animation-video-toolkit** — animation and video work.
- **agent-browser** — core browser automation: snapshot-and-ref workflow.
- **agent-browser-dogfood** — systematically explore a web app to find
  bugs and UX issues.
- **mcp-builder** — build MCP servers.
- **skill-creator** — create, improve and measure skills.

### Documents and research

- **docx** — create, edit and analyse Word documents.
- **pdf** — read, extract and work with PDF files.
- **xlsx** — create, edit and analyse spreadsheets.
- **grok_x_search** — search public X posts through the Grok Build CLI.
- **humanize-skills** — rewrite skill text to sound human.

## Bundled skills (58) — the general bench

### Build, publish, test

- **documents** — read, write and revise documents, PDFs, spreadsheets
  and presentations.
- **custom-connector-setup** — connect a service this agent does not
  bundle, through its API or MCP server.
- **file-hosting** — put a file where the right people can open it and
  return a safe link.
- **live-page-checks** — check a product's current price, stock or
  availability at a known store.
- **image-search** — search the web by text for image URLs and sources.
- **media-library** — search and inspect the photo library.
- **form-design** — design forms.
- **muse_db** — inspect the agent's own records with read-only SQL.

### Money, shopping, travel

- **shopping** — find, compare and buy real products (except groceries).
- **remember-products** — remember products the owner asked to save.
- **marketplaces** — buy, sell and value used items (eBay, Facebook
  Marketplace, Craigslist).
- **groceries** — groceries for delivery or pickup; takeout and prepared
  meals.
- **financial-planning** — budgets, affordability, debt repayment.
- **business-finance** — bookkeeping and invoicing.
- **mortgage-comparison** — compare mortgages.
- **store-operations** — run a store's day-to-day operations.
- **flight-booking** — find and book flights.
- **flight-tracking** — live flight status and trip monitoring.
- **hotel-booking** — compare and book places to stay.
- **trip-planning** — plan a trip as one living itinerary.
- **trip-transport** — rental cars, trains, ferries, buses, rides.
- **event-tickets** — find, compare and buy event tickets.
- **restaurant-reservations** — find a restaurant with a real available
  table, then book, change or cancel the reservation.
- **advertising-campaigns** — advertising campaigns.
- **customer-outreach** — reach out to customers.
- **smb-product-shots** — polish product photos for a shop listing.
- **style-tryon** — see clothing and accessories on the owner's photo.

### Communication and organisation

- **email-management** — find, triage, draft and send email.
- **wide-research** — research a question across many sources before
  answering it.
- **messaging** — message people from the owner's accounts.
- **scheduling** — find times across calendars and timezones; book
  appointments.
- **meeting-follow-up** — turn meeting notes into decisions and tasks.
- **knowledge-organization** — organise notes in Notion, Drive, Docs.
- **translation** — translate text.
- **transcribe-recordings** — transcribe audio or video.
- **spoken-audio** — voice notes and narration.
- **social-publishing** — publish to social accounts.
- **social-content-performance** — read how social posts performed.
- **share-ideas** — share ideas.
- **generate_podcast** — research, script and produce a podcast episode.
- **music-discovery** — find music, build playlists, start playback.

### Life, health, home

- **fitness-tracking** — activity, sleep, recovery and measurements
  against goals.
- **workout-planning** — plan workouts.
- **health-review** — organise health records for a clinician visit.
- **wearables-comms** — calls and texts from glasses.
- **home-control** — control home devices and routines.
- **home-search** — search for a home.
- **device-data** — read cached contacts and calendar from device sync.
- **place-discovery** — find and compare places to go.
- **goals** — create and accomplish goals.
- **task-management** — manage tasks.
- **proactive-work** — background proactive work.
- **self-awareness** — the agent's own self-knowledge.
- **forget** — remove information the owner asked to forget.
- **muse-early-access** — Muse's early access program.
- **muse-feedback** — feedback and feature requests to the Muse team.
- **subscription-status** — the Muse subscription, plan and usage.
- **avatar-dance-videos** — dancing videos for the agent's avatar.

## How to read this index

- A skill is listed here because it is installed. Installation is not a
  claim that it was used: `SKILLS.md` says which ones the work in this
  repo actually runs on.
- Load a skill by reading its `SKILL.md` first. The name is not the
  instructions, and a skill's defaults are not the owner's decisions.
- When a job needs a skill that is not here, the move is to build one
  (`skill-creator`) or connect the service (`custom-connector-setup`),
  not to pretend the skill exists.
