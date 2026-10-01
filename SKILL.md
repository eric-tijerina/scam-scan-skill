---
name: "scam-scan"
description: "Smell-test any money opportunity (bounty, arena, airdrop, investment, paid gig) for scam signals before anyone spends a cent. Scores red flags, does the prize-vs-deposit math, and returns a verdict: CLEAN, CAUTION, or LIKELY SCAM. Trigger: is this a scam, scan this opportunity, smell test, should I trust this, check this bounty."
---

# Scam Scan

## Purpose
One job: look at a money opportunity the way a skeptical local looks at a carnival game — count what it costs, who holds the money, and how winners get picked — then say plainly whether it stinks.

## Workflow
1. **Gather the facts.** Get the listing page, announcement, or terms. What does it promise, what must you put in (money, sign-ins, posts, time), who holds deposited funds, how are winners chosen, when do they announce, and is there proof of past payouts? Use `bin/fetch-listing <url>` for a quick text pull, or the browser tools.
2. **Run the red-flag checklist** (`references/red-flags.md`). Mark each flag hit or clear, with the evidence quote.
3. **Do the math.** Total estimated cost to enter (deposits + fees + time) vs. your realistic share of the prize pool. If total player deposits dwarf the prizes, say so with numbers.
4. **Check the sponsor separately.** A legit platform (Superteam, etc.) does not vouch for the sponsor. Look for the sponsor's own track record and past payouts.
5. **Return the verdict** per the Output Contract below.

## Output Contract
- **Verdict:** one of `CLEAN`, `CAUTION`, or `LIKELY SCAM`.
- **Score:** red flags hit, e.g. "4 of 10".
- **The math:** cost-to-enter vs. prize, in one or two lines.
- **Flags found:** each with the evidence (quote or fact).
- **Recommendation:** one line — enter, enter-with-limits, or walk away. Name the single biggest reason.
- Keep it short enough to read on a phone.

## Operating Rules
1. $0 spend applies to the scan itself — never deposit, sign in, or connect a wallet to investigate.
2. "Not an outright scam" is not a pass — bad economics (pay-to-play with negative expected value) gets CAUTION or worse on its own.
3. Never reveal the operator's internals in any public check (no posting questions about a listing from the operator's accounts).
4. When in doubt between CAUTION and LIKELY SCAM, pick LIKELY SCAM — false alarms are free, lost deposits aren't.
