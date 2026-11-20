# Tools behind the skills

The skills in this kit call real programs. This file lists the ones this agent actually uses, the versions tested, where to get each one, and the known problems. Install only the tools for the skills you plan to use.

## make.fun

- **The kit CLI** — `node cli/makefun.mjs`, shipped with each bounty kit. Commands: `login`, `register`, `bundle`, `check`, `submit`, `status`, `claim`, `referrals`. Needs Node.js 22. Kits are versioned — always download a fresh kit, because the site moves on and an old kit's rules go stale.
- **The agent keypair** — created by the first `login`, kept at mode 600, never printed, never sent anywhere. It is the account and the payout wallet at once.
- **API auth** — the make.fun API takes an `x-api-key` header. A Bearer token is rejected.
- **Never run `makefun compress` on a TypeScript entry.** It emits a Python stub and the grade goes to zero. It is fine on Python.
- **Local scores do not predict server scores.** Quote a local score only with that warning attached.

## On-chain — Binance agentic wallet and minting

- **`baw` CLI v1.12.0** — lives at `~/workspace/.local/node_modules/.bin/baw` and is **not** on the default PATH. Prepend that directory before use, or every wallet call reports UNKNOWN.
- **Sign-in flow** — `baw auth signin --json` prints a pairing code and a URL; the owner confirms in the Binance App; `baw auth verify --qrCodeId <id> --json` blocks for up to about five minutes. A pairing code lives about five minutes, and on rejection you start over with a fresh sign-in.
- **Source of truth** — `baw wallet status --json`, not the App screen.
- **fastmint** — `fastmint.sh` wraps the bench, recon, fire, logs, and locks scripts. Run everything through `fastmint.sh`, never `fire.js` or `bench.js` directly — the wrapper is what puts `baw` on the PATH. Measured on this machine: preview about 1.1–1.4s, broadcast about T+2.4s, included about T+2.9s.
- **Foundry 1.9.0** — at `~/.foundry/bin`. Used for fork tests and proof-of-concept runs.
- **Blockscout API** — the chain explorer API for reading logs. Note that `ethereum-rpc.publicnode.com` rejects `eth_getLogs`, and Blockscout's API is Cloudflare-blocked from this machine, so read logs with `cast logs` in 100k-block chunks instead.

## Bug bounty — recon and hunting

- **`bughunter` CLI** — at `~/.local/bin/bughunter`. It is a **wrapper script** that unsets `no_proxy` and `NO_PROXY` before running the engine. Do **not** replace it with the plain symlink from the install script: this machine's `NO_PROXY` holds bracketed IPv6 entries that crash the HTTP client on every AI command.
- **Go 1.27.4** — at `~/workspace/.local/go/bin/go`. Recon tools in `~/.local/bin`: subfinder, httpx, nuclei (+ templates), ffuf, amass, gau, dalfox, subjack, sisakulint. nmap via apt at `/usr/bin/nmap`.
- **Groq** — provider `groq`, model `openai/gpt-oss-20b`, key held in the secure vault. Used by the bug-hunter engine for triage and drafting.
- **Go recon TLS is broken through the egress proxy** — curl and Python work where the Go tools fail. That is a proxy problem, not a target problem.
- **Datacenter-IP egress** — shared IPs get 403s from some WAFs (Coupang, OPPO) and aggressive 429s from others. A single 429 or failed read is never evidence of absence.

## Browser

- **agent-browser CLI** — the published CLI is gone from `/usr/bin` on this machine. The Chrome 157 binary still lives at `~/.agent-browser/browsers/chrome-157.0.8103.78/chrome` — drive it directly with a Node CDP script when the CLI is absent.
- **Guardrails** — always restrict `--allowed-domains` and require `--confirm-actions` on untrusted pages. The browser auth vault must never hold seed phrases or private keys.
- **Cloud-browser clipboard does not reach a phone.** Never ask the owner to copy from it; have them copy and paste in Chrome on their own phone instead.
- **X blocks the cloud browser outright** (403 bot wall). Do not promise to read posts from the browser; the make.fun server reads them fine.

## Machine quirks

- **`/tmp` is 100% full** (a 512M tmpfs). Installers, clones, and anything that writes temp files must use `TMPDIR=$HOME/workspace/tmp-install`, or they fail with a tar error. Home disk has roughly 143G free.
- **No Homebrew on this machine.** Do not run install scripts that assume it.
- **Secrets live in the secure vault or the approved connection flow.** Passwords and API keys are collected on secure pages, never in chat. A one-time code is passed by its reference, never unwrapped or repeated.
