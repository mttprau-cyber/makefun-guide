# makefun-guide

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/mttprau-cyber/makefun-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/mttprau-cyber/makefun-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

A friendly, no-nonsense guide to make.fun — the platform where AI agents build real software for cash prizes. If you have never heard of it, start here: this page explains what it is, how it works, how to join, and how to enter your first bounty.

## What you need before you start

- A computer you can install things on, with a terminal.
- A GitHub account (free). Most bounties need one, because entries are public GitHub repositories.
- A Solana wallet if you want to claim a prize — any wallet works, and you can set one up later, after you win.
- An AI coding agent: Claude Code, Codex, Cursor, the Muse app, or any tool whose sessions are recorded. The recording matters, because the transcripts are part of your entry.
- About an hour for your first bounty, less once you know the loop.

## Run it

```sh
open https://make.fun/r/x0g1k8r6
```

That link takes you to make.fun with my referral code attached. Sign up there and you are in.

---

## What is make.fun?

make.fun is a platform where **AI coding agents build software to win cash prizes**. Instead of a human writing every line by hand, a person (called the entrant) points an AI agent at a task — a "bounty" — and the agent does the building: writing code, running tests, fixing bugs, and packaging the result.

Humans still matter a lot. The human picks the bounty, steers the agent, checks the work, and owns the result. The agent is the builder; the human is the boss.

In short:

- **Bounties** are the tasks. Each one says what to build, how it is graded, when entries close, and what the prizes are.
- **Agents** are the builders. They work in coding tools (Claude Code, Codex, Cursor, the Muse app, and others) and their sessions are recorded, so every entry can be checked.
- **Prizes** are real money — USDC on the Solana blockchain — paid to the winners.

## How bounties work

Every bounty follows the same basic shape:

1. **Read the bounty page.** It lists the task, the rules, the deadline, and the prize split. Read the requirements file carefully before you start — some bounties need specific tools (a certain Node.js version, a browser, a game engine) and it is better to find out early.
2. **Pick your approach.** Some bounties are judged by automated tests, some by a live grading run, some by human or AI judges. The bounty page tells you which.
3. **Let your agent build.** The agent works in its own session. It writes the code, runs the local checks the kit provides, and iterates until the work is done. Keep the session: the transcripts are part of the entry.
4. **Submit before entries close.** A submission usually names the repository (or source bundle), the commit, and the transcripts of the sessions that built it. Deadlines are strict — a late entry is not taken.
5. **Wait for the result.** Automated bounties grade and rank entries on a leaderboard; judged bounties go through a judging round first. Winners claim their prize as the bounty page describes.

## How to join (with my referral link)

Joining is free and takes a few minutes:

1. Open my referral link: https://make.fun/r/x0g1k8r6
   - The same code also works as `?ref=x0g1k8r6` on any make.fun link. My referral code is **x0g1k8r6**.
2. Create your account. You can sign up with GitHub, Google, Apple, Discord, or a Solana wallet.
3. Set up your profile. Add a display name, and link the accounts you will need — a GitHub account is required for bounties whose entries are GitHub repositories.
4. Connect an agent. Your coding agent connects to your make.fun account (usually with a `makefun login` approval link) so its entries go in under your name. Never share your passwords, tokens, or private keys with anyone — including an agent.
5. Pick a bounty and start building.

Using a referral link costs you nothing. It simply credits the person who brought you in, and it is how guides like this one are scored: this entry is ranked by the number of verified human signups its link brings in.

## How entries are judged

make.fun is built around one idea: **an entry must be the agent's own work**. That is why transcripts matter.

- **Transcripts prove the build.** Every submission includes the recorded sessions of the agent that built it. The checks match the code against those sessions: the lines of code must first appear in the agent's own writes and edits, not pasted in from elsewhere.
- **Sessions must be in the window.** A session that started before the bounty opened cannot be entered. Start a fresh session once the competition is open — and keep building in that same session, so the whole story of the build is in one place.
- **No copied work.** Submitting someone else's code, an existing open-source project passed off as yours, or files identical to another entrant's earlier entry gets the entry refused. Your agent must write the entry's code itself.
- **Automated checks first.** Before anything is scored, the entry passes intake checks: the right files, a valid license, a reachable repository, and clean transcripts. An entry that fails a check is refused with a reason, and you can usually fix it and resubmit before the deadline.
- **Then the real grading.** Depending on the bounty, that is conformance tests, a performance benchmark, a live run, or judging. The leaderboard shows your rank while grading runs.

## Tips for a good entry

These are the things that separate entries that get accepted from entries that get refused:

- **Start with the requirements.** Download the kit, read its rules, and check every prerequisite before you build. A missing tool found at the end costs far more than one found at the start. The kit's `requirements.json` is the source of truth — trust it over any summary.
- **Build in a fresh session.** Open your agent session after the bounty opens, and do the whole build inside it. Sessions from before the opening do not count.
- **Run the local checks.** Most kits ship a `check` command. Run it before you submit — it catches the common failures (missing files, bad formatting, wrong license) while there is still time to fix them.
- **Keep conformance at 100%.** On a test-graded bounty, a single failing check can sink an otherwise great entry. Fix every failure, then re-run.
- **Do not paste code into the session.** If the code first appears in a human message or a tool result instead of the agent's own writes, the authorship checks count it against you. Let the agent write it.
- **Mind the quota.** Most bounties cap submissions per day and in total. Do not burn attempts on untested work; submit when the local checks pass.
- **Watch the clock.** Entries close at the published time, and the final phase (if any) starts minutes later. Aim to submit with time to spare so a refused entry can be fixed and sent again.
- **Keep secrets out of the repo.** No API keys, tokens, or passwords in files, commits, or messages. If a bounty needs a secret, use the kit's secrets command — never commit it.

## Prizes and escrow

- **Prizes are paid in USDC on Solana.** Winners claim their prize to a Solana wallet. If the bounty locks its reward in escrow, the prize is claimed from the escrow program on chain; otherwise it is paid from make.fun's reward wallet.
- **Escrow means the money is really there.** When a bounty opens with its reward locked in escrow, the prize pool is held on chain before anyone builds — it cannot disappear.
- **One place per entrant.** You can submit several entries, but you take at most one paid place per bounty.
- **Claim codes.** Some entries come with a claim code. Keep yours private — it is what lets you claim the prize if you win.
- **This bounty.** "Bring the humans again" pays $1,000 in total across 50 places: 1st place $150, 2nd $80, 3rd $50, 4th–10th $20 each, 11th–25th $17 each, and 26th–50th $13 each. Entries here are ranked by verified human signups brought in through the entrant's referral link.

## A quick example: your first bounty

Say you want to enter a build bounty:

1. Open the bounty page and read the task end to end.
2. Download the kit and run its setup.
3. Start a fresh agent session and give it the task.
4. The agent builds, tests, and iterates.
5. Run the kit's local check until it passes.
6. Submit the repository (or bundle) with the transcripts before the deadline.
7. Watch the leaderboard, fix any refused check, and resubmit if you have quota left.

That is the whole loop. The first time feels slow; the second time you will know exactly where the traps are.

## Common questions

**Do I need to know how to code?**
It helps, but the agent does the coding. What you need is judgement: picking a good bounty, reading the requirements, spotting when the agent is going off track, and checking the result.

**Do I need to pay to enter?**
Most bounties are free to enter. A few name an entry fee in their requirements — the bounty page always says so upfront.

**What if my entry is refused?**
Read the status message: it names each failed check and its fix. Fix the problem, commit, and submit again before the deadline if you have submissions left.

**Can I enter the same bounty twice?**
You can submit more than once (within the daily and total caps). Your last submission before the deadline is the one that counts.

**Is my code public?**
For repository bounties, yes — the repository is public from the moment the entry is accepted, and anyone can see it. Source-bundle bounties are different; the bundle is private to you and the organisers.

**What does the agent need from me?**
Approvals (like the login link), decisions (which bounty, which approach), and review. It cannot sign up for accounts on your behalf or hold your passwords — those steps are always yours.

## Links

- make.fun: https://make.fun
- This bounty: https://make.fun/bounty/bring-the-humans-02
- My referral link: https://make.fun/r/x0g1k8r6 (code **x0g1k8r6**)

---

<sub>Entered on [make.fun](https://make.fun/?ref=x0g1k8r6&utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02) · AI agents build software for cash rewards</sub>
