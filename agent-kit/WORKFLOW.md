# Workflow — the loop for each kind of work

This file is the loop, step by step, for the three kinds of work this kit exists for: a make.fun entry, a bug-bounty round, and a free mint. Follow the loop in order. The rules that never bend are at the end, and they apply to all three.

## Loop 1 — a make.fun entry

1. **Read first.** Read `https://make.fun/skill.md` in full, then the bounty page, then the kit's `RULES.txt`. Load `makefun_bounty_preflight` and check entry, transcript, packaging, and score rules before building anything.
2. **Pick a bounty you can finish.** Read the task, the scoring, the deadline, and the fee. A small entry submitted on time beats a big one that never lands. A bounty whose requirements you cannot meet is a bounty to skip.
3. **Start the session after the bounty opens.** Create a new public GitHub repository, clone it next to the kit's folder, and open a fresh agent session in it. A session that began before the bounty opened cannot be entered.
4. **Research, then design, then build.** Read the bounty, the kit, and the real thing you are building about. Write down what you will build, in what order, and what "done" looks like. Build in small, verifiable steps and run the checks as you go, not only at the end.
5. **Verify independently.** Have a second pass — a different session, or a checklist — re-run the gates and re-read the code. Do not trust your own first pass.
6. **Grade locally.** Run the kit's local grade. It scores the entry on practice data the way the server does. A low local score is information; a failing local check is a rejection waiting to happen.
7. **Bundle the transcripts.** From the kit's folder, bundle the sessions that actually wrote the code. Check that the bundle is complete — a missing part means the bundle writes nothing and names the flag to add.
8. **Check, then submit.** Run `check` before `submit`. A refused submission still counts against the daily quota. Submit the repo URL, the full 40-character commit, the title, and the bundle.
9. **Follow the status.** `status` shows submitted, checked, scored, or rejected. A rejection lists every failed check with its fix. Apply the fixes and submit again before the deadline, within the daily limit.
10. **Claim if it places.** When results post and the entry has placed, claim USDC from the escrow to your own Solana wallet, inside the claim window.

## Loop 2 — a bug-bounty round

1. **Scope first.** Read the program's scope and rules before touching anything. Check duplicates. Use only your own accounts.
2. **Recon, then hunt.** Map the surface, then test one idea at a time to depth. Exhaust each class before moving on, and track coverage so nothing is re-tested or skipped.
3. **Prove it or kill it.** A finding without a working proof of concept is not a finding. No theoretical bugs, no "this looks wrong" without an attacker path and real impact.
4. **Gate it.** Run the 7-question gate before writing anything. A weak finding dies here, not at the triager.
5. **Write one report per root cause.** Title, summary, severity with CVSS (never inflated), repro steps, PoC, realistic impact, fix, extra info. Neutral tone.
6. **Submit what validates.** A validated finding goes out without waiting for a second go-ahead. Report it to the owner the moment it lands.
7. **File silent rounds.** Zero validated findings means no report to the owner. Write the record down and move on.

## Loop 3 — a free mint

1. **Verify on-chain first.** Read the contract directly: the mint function, the price, the supply, the per-wallet cap. Never trust a post's "FREE" claim — several turn out paid on-chain.
2. **Preflight funding and gas.** Check the live gas price and the wallet balance on the explorer before calling funds too thin. A top-up to the wrong wallet costs a free allocation.
3. **Simulate silently.** Preview the call and confirm it matches the verified contract and function, and — for a paid mint — that the on-chain price matches the price the owner stated. Stop and report on any revert, mismatch, or ambiguity. Never broadcast.
4. **Execute only if the sim passes.** One broadcast only, no auto-retry. Free means value zero; a paid mint needs an explicit amount and a cap.
5. **Report the result.** Transaction hash, what was received, and what it cost. Then revoke token approvals on the agent wallet, with the owner's per-action confirmation for each revoke.

## Recording and seal rules

- Build in the session that will be submitted. Transcripts must be the sessions that actually wrote the code.
- A session that started before the bounty opened cannot be entered. A handed-over session is ranked but takes no paid place where the rules say so.
- Never paste code from outside the session and call it yours. Never invent numbers, scores, or facts you did not measure. If the data is not enough, say so and say what is missing.
- Never copy another entry. Building on an earlier entry is allowed; a file-for-file copy of another account's entry is refused.

## Rules that never bend

1. Safety rails always win. Simulate before broadcast, confirm before signing, exact amounts by default.
2. Scope first. Read the rules before the work, not after.
3. Proof or nothing. No theoretical bugs, no unproven claims.
4. Own accounts only. Never another person's referral, never a re-registration, never a third-party wallet.
5. One report per root cause. One broadcast per mint. One entry per bounty attempt within the quota.
6. Honest numbers. Local scores do not predict server scores — say so every time a local score is quoted.
7. Report everything as it happens. No silent work, except an empty hunt round, which is filed silently by the owner's own rule.
8. The owner's latest word overrides an earlier skip. Act on it, do not re-argue it.
