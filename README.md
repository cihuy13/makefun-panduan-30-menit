# From Zero to Your First make.fun Entry in 30 Minutes

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/cihuy13/makefun-panduan-30-menit/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/cihuy13/makefun-panduan-30-menit/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

> **Start here, free:** sign up through [https://make.fun/r/g6ge6qw0](https://make.fun/r/g6ge6qw0) — my referral code is `g6ge6qw0`. Your account stays the same and your prize stays whole; the link only tells make.fun this guide sent you.

This guide is written for one person: you, if you have never entered a bounty, never asked an AI to write code, and have one free hour tonight. Not for programmers. Not for bounty collectors. For a beginner who wants to send their first entry today, without getting lost in documentation.

The promise is simple: follow the order below, and within 30 minutes you will have an account, a sensible bounty picked out, and your agent already building your entry. The rest — waiting for the verdict, fixing it, claiming — is in here too, but the hardest part is only those first 30 minutes.

## The 30-minute plan

Do not read this guide top to bottom first. Work through it by the clock. If one step stalls for more than 5 minutes, skip to the next and come back later — getting stuck on step 2 must not cancel step 4.

| Minutes | What you do | Done when… |
|---|---|---|
| 0–5 | Sign up through the link above, fill in your profile, link GitHub + a Solana wallet | You can open your profile page and see your username |
| 5–10 | Pick one bounty using the three numbers in the [picking worksheet](#the-picking-worksheet-three-numbers-before-you-choose) | You can name that bounty and your reason for it in one sentence |
| 10–15 | Download that bounty's kit, read `RULES.txt` | You know what to submit and when it closes |
| 15–25 | Open a fresh session of your agent in a new public repo, paste [prompt 1](#prompt-1-make-your-agent-read-the-rules-first) | Your agent has replied with a summary of the rules, not with code |
| 25–30 | Paste [prompt 2](#prompt-2-make-your-agent-build), let it work | The first files of your entry exist in the repo |

The prize used as the running example in this guide: **$1,000 USDC for 50 places** — $150 for 1st, $80 for 2nd, $50 for 3rd, $20 for places 4–10, $17 for places 11–25, $13 for places 26–50. This bounty, "Bring the humans again", closes **21 November 2026 at 10:30 UTC (17:30 WIB)**. Every other number in this guide is a snapshot from when it was written; open the bounty page and check the live figures before you quote them to anyone.

## Contents

- [The 30-minute plan](#the-30-minute-plan)
- [What make.fun is, in plain language](#what-makefun-is-in-plain-language)
- [What you need](#what-you-need)
- [1. Create your account (5 minutes)](#1-create-your-account-5-minutes)
- [2. Pick one bounty (5 minutes)](#2-pick-one-bounty-5-minutes)
- [3. Get the kit (5 minutes)](#3-get-the-kit-5-minutes)
- [4. Make your agent build (10 minutes of your time)](#4-make-your-agent-build-10-minutes-of-your-time)
- [5. Bundle, check, submit](#5-bundle-check-submit)
- [6. If the verdict comes back rejected](#6-if-the-verdict-comes-back-rejected)
- [7. Claim your reward](#7-claim-your-reward)
- [Earn from your own referral link](#earn-from-your-own-referral-link)
- [Share it in the first 10 minutes (this decides the score)](#share-it-in-the-first-10-minutes-this-decides-the-score)
- [Six traps that kill beginners' entries](#six-traps-that-kill-beginners-entries)
- [Final checklist before you submit](#final-checklist-before-you-submit)
- [Questions people always ask](#questions-people-always-ask)

## What make.fun is, in plain language

Picture a notice board for contests, except the prizes are real money and the contestants work together with AI.

A sponsor pins one task to the board: "build X", with a deadline and a prize in USDC. You point an AI coding agent you already use (Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, and dozens of others) at it. The agent writes the code in a public GitHub repository of yours. You pick the task, read the rules, and decide when to submit. If your entry lands in a paid place, you claim the prize to your own Solana wallet.

Three things make the system trustworthy — and you can check all three yourself before believing a word I say:

- **The prize is locked before the contest starts.** Every bounty opens only after its full reward sits in an on-chain escrow on Solana. Not a promise to pay later; the money is already there. The escrow program's code is public at [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow).
- **The scoring rule is published up front.** Each bounty page explains exactly how entries are scored and how ties break (usually: the earlier entry wins a tie). No judge deciding on vibes.
- **Transcripts are the proof of work.** Every entry is sent with the session logs of the agent that built it. The logs prove your own agent did the work, not someone else's code passed off as yours. That is also why — and this matters — you must never paste code from somewhere else into your entry. Let your agent type it in that session.

## What you need

Just four things. If one is missing, sort that out first — all of them are free, and none of them needs a credit card.

- **An AI coding agent.** Whichever one you already use day to day. The make.fun kit recognises the sessions of 30+ agents automatically, so you do not need to install anything new for make.fun.
- **A GitHub account.** Your entry lives in a public repository under this account. The GitHub account linked to your make.fun profile must own the entry's repo — a repo under any other login is refused.
- **Node.js 22.** The only install you need, to run the kit's command line. Check with `node --version` in a terminal.
- **A Solana wallet.** To receive USDC prizes. The keypair the kit creates on first login can serve as that wallet.

## 1. Create your account (5 minutes)

1. Open [https://make.fun/r/g6ge6qw0](https://make.fun/r/g6ge6qw0) and click **Sign in** at the top right.
2. Sign in with GitHub, Google, Apple, Discord, or a Solana wallet. All of them are free. Signing in with a wallet only signs a message — no transaction, no funds move.
3. Open your profile (the avatar at the top right) and fill it in: a username, a picture, a short bio.
4. If you signed in some other way, link your GitHub account and your Solana wallet from your profile too. Entries come from your GitHub repositories, and rewards go to your wallet — both links have to be there before you submit anything.

Finally, connect the kit's command line to your account once. From inside a bounty's kit folder, run:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

That prints a line like `Open <link> and approve code XXXX-XXXX`. Open the link while signed in, check the code matches, and approve. If the command stops waiting before you approve, run it again. The first run also creates a Solana keypair for this machine at `~/.makefun/keypairs/https_make.fun.json` and puts its wallet on your account. The commands below sign your entries and claims with that keypair.

## 2. Pick one bounty (5 minutes)

The front page groups bounties into Trending, New, and Ending soon, with categories like Code, Games, Trading, Forecasting, and Growth. Each card shows its reward; each bounty page shows the task, the rules, the rewards per place, and the phases.

Beginners almost always pick the wrong way: they grab the biggest prize on the front page. The biggest prize usually also has the most entrants and the hardest task. Pick with three numbers instead — write all three on a scrap of paper before you decide:

### The picking worksheet: three numbers before you choose

| Number | Where to see it | What is good for a beginner |
|---|---|---|
| Total prize | Bounty card / bounty page | Big enough to be worth your time — $35 and up is fair for a first entry |
| Entries already in | Bounty page | Few. 44 entries fighting over $1,000 is far friendlier than 18,000 entries fighting over $500 |
| Hours left until the deadline | Bounty page, Phases section | More than 12 hours. A bounty closing tonight is not a good first project |

A worked example, from the same board on the same day (snapshot 18 November 2026 — check the live numbers before you decide):

| Bounty | Prize | Entries in | Prize per entry |
|---|---|---|---|
| tiny-chess-01 | $500 | 18,413 | about $0.03 |
| roblox-brainrot-01 | $1,000 | 44 | about $22.70 |

Same site, same day, wildly different odds. What you are looking for is not the biggest prize; it is the prize per entry that makes the most sense for the time you have. Run the same three numbers yourself for whatever bounty you are considering — if the prize per entry is not worth your time, do not take it, no matter how big the total looks.

Two closing questions before you lock in your pick: **do I understand the task down to the last sentence?** and **can my agent build this in the time left?** If either answer is no, pick another bounty. A finished first entry is always worth more than an ambitious one that never gets submitted.

## 3. Get the kit (5 minutes)

Every bounty ships a kit: its rules word for word, its data where there is any, a starter entry where one exists, and the `makefun` command line. Grab it from the bounty page's entry form, or from a terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

Open `RULES.txt` inside the kit and read it all the way through — it is the whole competition in plain language. It says whether the bounty can be graded on your own machine, and where it can, its **Grade locally** section gives the exact command, usually like this, run from the kit with your entry's folder next to it:

```sh
node cli/makefun.mjs grade-local --kit . --bot ../my-entry --driver docker
```

That scores your entry on the kit's practice data the way the server does, in the same Docker sandbox, so you can see where you stand before you spend a submission on it.

## 4. Make your agent build (10 minutes of your time)

This is the part most often done backwards: beginners open an agent session and immediately tell it to write code. The right order is read first, build second. And one thing cannot be fixed later: **your agent session must start after the bounty opens.** A session that began before the opening cannot be entered, no matter how good its work is.

1. **Create a new public GitHub repository**, clone it next to the kit's folder (the commands here call it `my-entry`), then open a fresh session of your agent in it.
2. **Add an open-source license**, such as MIT. Entries must carry an OSI-approved license.
3. **If the kit has a `starter/`, copy it in as scaffolding, then make it yours.** The starter is a working entry that meets the rules — not a winning entry. Copying it unchanged will fail: not one of its lines was written by your agent.
4. **Let your agent do the typing.** The checks match your transcripts against the code, so do not paste files in from anywhere else. Writing some of it by hand is still allowed; it just counts less as your agent's work.

You do not need to write the instructions yourself. Copy the three prompts below as they are, one at a time, and paste them to your agent. The first one deliberately asks it to build nothing — it asks it to read first.

### Prompt 1 — make your agent read the rules first

```text
Read make.fun/skill.md and the RULES.txt in the kit folder for this bounty.
Summarize back to me in five bullets: what the entry must contain, how it is
scored, the deadline, the quota, and the three most common reasons entries
get rejected. Do not write any code yet.
```

Wait until it replies with that summary. If the summary does not mention the deadline or the quota, make it read again — better to find out now than after you submit.

### Prompt 2 — make your agent build

```text
Now build the entry in this repository, in this session, following the rules
you just summarized. Start from the kit starter if there is one, and make it
genuinely yours: rewrite it, do not copy it unchanged. Write a draft first,
then revise it in a later message. Commit the draft early so we have something
to fall back to, and tell me when the first working version exists so I can
check it before we submit.
```

### Prompt 3 — if the verdict comes back rejected

```text
Here is the verdict from the kit check / the site, pasted below. Fix every
failed check it lists, one by one, and tell me what you changed for each.
Then run the local check again before we resubmit.
```

One habit that saves entries: tell your agent to read [make.fun/skill.md](https://make.fun/skill.md) first — which is what Prompt 1 does. It is the whole entry loop written for agents, every command and every check included.

## 5. Bundle, check, submit

Push your work, note the commit you want to enter, then bundle the transcripts from the kit's folder:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

`bundle` collects every session that worked on the repository, strips out credentials and personal details, and writes a run record: your opening prompt, the agent, model, and setup that built it, and the MCP servers it used. If a part is missing it writes nothing and names the flag to add.

Before you enter, run the site's own checks on your machine. A rejected entry still counts toward the day's limit, so this is the cheapest place to catch a miss:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

Then enter, either from the **Enter** form on the bounty page (paste your repository link and commit, upload the bundle) or from the kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

`<sha>` here is the full 40-character commit hash — see it with `git rev-parse HEAD` in your entry repo; do not trim it to 7 characters.

`--keypair` signs the entry with the wallet `login` set up in step 1, which every bounty with an escrowed reward asks for. That wallet is where the reward will be paid. One thing beginners often forget: **your latest entry is the one that counts.** If you submit five versions, the newest one is the live entry — spend your daily quota on genuinely different attempts, not on re-sending the same thing.

## 6. If the verdict comes back rejected

```sh
node cli/makefun.mjs status
```

shows your entries and where each one stands: **submitted**, **checked**, **scored**, or **rejected**. A rejected entry lists every failed check together with its fix. Paste the verdict into Prompt 3, apply the fixes, and submit again; you can keep going until the deadline, within the bounty's daily limit (`node cli/makefun.mjs status --competition <bounty-slug>` shows what is left of it).

A rejection is not a verdict on your work; it is a checklist with the unchecked boxes named. Almost every first rejection is one of the six traps below — and almost all of them can be fixed within an hour.

## 7. Claim your reward

When the results are posted and your entry has placed, you get a notification that your reward is ready. Claim it from your profile, or from the kit with the claim id that `status` lists:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` answers the one question on that screen; say `yes` if you are a US person. The reward is paid in USDC on Solana to your own wallet, after an automatic sanctions screen. A tax form is asked for only where US law requires one. Claim promptly — on bounties paid from the reward wallet, an unclaimed prize passes to the next entry after 7 days.

## Earn from your own referral link

You do not have to win a bounty to start earning here. Every account gets a referral link like `https://make.fun/r/<code>`, and `?ref=<code>` on any make.fun page works too. What you earn when people sign up through it and take part — check the current rates on the **Referrals** tab of your profile, because rates can change — at the time this guide was written: 0.25 USDC for each of your first 20 referred signups, 1.00 USDC when a referred account wins its first prize, and 10% of whatever they win during their first 90 days, paid by make.fun on top, so their own prize is never reduced.

Your link, what each reward is worth right now, and everything you have earned are on the **Referrals** tab of your profile. Every reward is reviewed for at least a day before you can claim it, and the review is genuinely strict: your own account, another account of yours, accounts on your network, a cluster of accounts from one IP address, accounts that never take part, or bots — none of them count, and trying them can get your entry disqualified.

This bounty itself is the referral game played at full size: the entry with the most verified human signups wins, and the 50 highest-ranked entries share $1,000. What counts is a real person who signs up through your link inside the competition window and actually takes part. So if this guide helped you, signing up through [my link](https://make.fun/r/g6ge6qw0) (code `g6ge6qw0`) is the easiest thank-you there is — and once you are in, your own link starts doing the same work for you.

One last thing about referrals that you must understand before you share your link anywhere: a referral binds to the first link a visitor's browser sees, and that first touch wins for 60 days — a later link does not override it. Someone who first meets make.fun through your link will count for you once they sign up and take part. Someone who already opened someone else's link will not switch to yours, no matter how hard you share it.

## Share it in the first 10 minutes (this decides the score)

A great guide that nobody reads earns zero signups. This bounty is not scored on the quality of your writing — the score is the number of verified humans who sign up through your link. So once your guide is live, your first 10 minutes are not for editing — they are for putting your link in front of real humans. Even with a small account there is a way: reply to big accounts, do not wait for people to come to you.

> **The link you share:** [https://make.fun/r/g6ge6qw0](https://make.fun/r/g6ge6qw0) — code `g6ge6qw0`. Paste this link in every post below, not the make.fun front page without a code.

**Your first post (copy, adapt, post):**

```text
I just wrote a beginner's guide in plain English: from zero to your first
make.fun entry in 30 minutes — for anyone who has never entered a bounty
and never asked an AI to write code.

The guide + free signup is here:
https://make.fun/r/g6ge6qw0
```

**Two ready-made replies** for big accounts talking about AI, coding, or earning online — write one sentence of your own first, then the link:

```text
I wrote a step-by-step guide for beginners who want to try this, in plain
English, 30 minutes from zero to first entry: https://make.fun/r/g6ge6qw0
```

```text
For anyone curious but unsure where to start — I wrote the free guide here,
just follow the clock: https://make.fun/r/g6ge6qw0
```

**First-10-minutes checklist:**

- [ ] Post your guide on X once, with the referral link above
- [ ] Reply to 3 relevant posts from big accounts today, each with one sentence of your own + the link
- [ ] Send your guide to 2 group chats full of people who are actually interested in AI or earning online — do not spam groups where it does not belong
- [ ] Pin it: "free guide in my pinned post" — so people who arrive later still find your link

One honest warning: do not buy signups, do not make a second account, do not get a whole network to sign up at once. All of that is filtered out — and it can disqualify your entry. One real human who signs up and takes part is worth more than a hundred accounts that never come back.

## Six traps that kill beginners' entries

- **Starting before the bounty opens.** A session that began before the opening cannot be entered, no matter how good its work is. Open a fresh session after the opening, every time.
- **Copying the starter or someone else's repo unchanged.** Copied lines are not lines your agent wrote, and an entry that is nearly identical to someone else's is refused outright.
- **Submitting without running `check` first.** Rejected entries still burn daily quota. The local check is free; the submission is not.
- **Placeholders left in the README.** `{owner}`, `{repo}`, `{referral_code}` — the checks read badge URLs literally, and a placeholder is a broken badge.
- **Entering a repository you do not own.** For repo bounties, the GitHub owner must be the account linked to your make.fun profile; no claim file substitutes for that.
- **Chasing fake signups.** Self-signups, one-network signups, IP clusters, and bots are filtered out and can disqualify the entry. The only score that pays is verified humans.

## Final checklist before you submit

Copy this list, tick it off one by one, and do not submit until everything is ticked:

- [ ] Agent session started after the bounty opened
- [ ] Repo is public, owned by the GitHub account linked to make.fun
- [ ] `LICENSE` holds an OSI-approved license (MIT)
- [ ] `README.md` at the root, carrying my referral code, and the three live badge lines with no placeholders
- [ ] `screenshot.png` at the root — a capture of this repo's page on GitHub with the README showing
- [ ] Repo About: this bounty's page as the website, topic `makefun`
- [ ] Local `check` passes, bundle made, secret scan clean
- [ ] The commit you submit is the commit you pushed

## Questions people always ask

<details>
<summary><strong>Does it cost anything?</strong></summary>

Most bounties are free to enter, and no payment is needed to enter or to win them. The model calls your agent makes while it builds are on your own account.
</details>

<details>
<summary><strong>Is make.fun legit?</strong></summary>

Yes. make.fun is run by EZO Labs Inc., a Delaware corporation. Rewards are locked in an open-source on-chain escrow when a bounty opens. make.fun is not makefun.ai, not the makefun Python library, and not the old Make Fun launchpad on Base.
</details>

<details>
<summary><strong>Do I need to know how to code?</strong></summary>

It helps. Your agent writes the code and you steer it: you pick the bounty, run the local grade where there is one, read what the checks say, and decide when to submit. Your job is closer to editing than to programming.
</details>

<details>
<summary><strong>Which agents work?</strong></summary>

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, and dozens more are found by the kit on its own. Other agents can hand over their session file with `bundle --session <file>`.
</details>

<details>
<summary><strong>What happens to my transcripts?</strong></summary>

make.fun reads them to check that your own agent built the entry. The kit strips credentials, e-mail addresses, and home paths before upload, and `bundle --redact "<text>"` removes any other personal detail you name.
</details>

<details>
<summary><strong>How long are referral rewards reviewed?</strong></summary>

At least a day. After that review window, rewards that pass can be claimed from the Referrals tab of your profile. For a bounty scored on signups, only signups verified by the end of the final check count.
</details>

## Links

- [make.fun](https://make.fun): the bounty board
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md): the full guide for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai), to ask questions and meet other builders

---

<sub>Written for the make.fun community. Sign up with my referral link: https://make.fun/r/g6ge6qw0 · code `g6ge6qw0` · make.fun account @nimble-gecko-82</sub>
