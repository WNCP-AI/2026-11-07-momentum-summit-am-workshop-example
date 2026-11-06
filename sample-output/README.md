# Sample output

> **FICTIONAL DEMO DATA.** The drafts and meeting notes come from the invented deal in `../CAST.md`. The news items
> are real and sourced. Nothing here was sent to anyone.

This is what the OS wrote from `../inputs/` and live news. It shows what the demo should produce.

## The run

- **Date:** 2026-11-04.
- **Harness:** Claude Code, in a scratch folder outside this repo: a fresh copy of `agentic-os/`, with `inputs/`
  next to it.
- **Model:** Claude Opus 5.5 (`claude-opus-5-5`).
- **Steps:** `onboarding`, then `outreach-setup` J1 to J7 in investor mode. Contacts came from `inputs/contacts.csv`
  and meeting notes from `inputs/meetings/`. Setup answers came from `../CAST.md`. Defaults were taken everywhere
  else, except one change in J6 (below).
- **News:** the harness's built-in web search, 90-day window. Result pages were opened to check dates.
- **Contacts:** Avery Fictional, Riley Madeup and Morgan Fakely. They are the first three by the default priority:
  Stage "Warm", then oldest Last touch.

## What is here

| Folder | Holds | Where the OS saved it |
|---|---|---|
| `drafts/` | The three follow-up drafts | `1_Work_Projects/2026.11.04 Outreach/drafts/` |
| `news/` | The news items `outreach-news` saved, labelled `yes` or `maybe` | `2_Research/News/2026/11/` |
| `meetings/` | The call notes `outreach-history` saved, five per contact | `1_Work_Projects/2026.11.04 Outreach/meetings/` |

Paths inside the drafts are the OS's own paths, from the third column.

## The drafts and their sources

| Draft | Past conversation it builds on | News item it cites |
|---|---|---|
| `drafts/2026-11-04 Avery Fictional.md` | 2026-10-28 leadership call: data room and term outline due 2026-11-06, Claude as default model open. `meetings/2026-10-28 Avery Fictional - Leadership call and next steps.md` | 2026-11-03, Hg invests in a new Claude transformation company for Europe, with Anthropic taking part. [PR Newswire](https://www.prnewswire.co.uk/news-releases/new-ai-transformation-company-raises-funding-to-advance-ai-adoption-in-europe-302927628.html) |
| `drafts/2026-11-04 Riley Madeup.md` | 2026-10-14 leadership call and the 2026-10-15 recap email: non-exclusive licence, OpenAI as government default. `meetings/2026-10-14 Riley Madeup - Leadership call on OpenAI versus rivals.md` | 2026-11-02, OpenAI appoints Dan Driscoll as Senior Counselor for National Security Modernization. [openai.com](https://openai.com/index/dan-driscoll-joins-openai/) |
| `drafts/2026-11-04 Morgan Fakely.md` | 2026-10-29 term sheet call: confirm by 2026-11-06, target 2026-11-20, lead slot held. `meetings/2026-10-29 Morgan Fakely - Term sheet timing.md` | 2026-10-21, Google Public Sector adds an FDE academy and $45M of deployment funding for partners. [Google Cloud blog](https://cloud.google.com/blog/topics/public-sector/google-public-sector-increases-partner-investments-for-frontline-adoption) |

Two drafts cite news newer than the contact's last call: Avery (2026-11-03, after 2026-10-28) and Riley (2026-11-02,
after 2026-10-14 and the 2026-10-15 email). Morgan's item is newer than the G2 call it relates to, but came out
before the last call on 2026-10-29. No call mentions it.

## Did the run find the live news on its own?

`../CAST.md` `## News` marks one event per lab `live: leave unused`. The run was not given them. The agent had read
`CAST.md` to answer setup questions, so it was not blind to them. It still had to reach each one through a search.

| Lab | Live event in CAST.md | Found by the run? | What the draft used |
|---|---|---|---|
| Anthropic | N-A6, 2026-11-03, Australian share offer (Reuters) | No. The search tool blocks reuters.com. It found the S-1 filing of 2026-10-26 on anthropic.com, labelled `maybe` | Hg and Anthropic, 2026-11-03. Not in CAST.md |
| OpenAI | N-O6, 2026-11-02, Dan Driscoll appointed | Yes, through a link on an openai.com page the search returned | N-O6 |
| Google | N-G6, 2026-11-04, US$15B Malaysia investment | Yes, top of the Google Cloud press list. Labelled `no`: data centres in Malaysia, not about GV and not a reason | Google Public Sector partner funding, 2026-10-21. Not in CAST.md |

## The one change in J6

The first run wrote one draft, for Avery, and left four items as `maybe`. The default reasons in
`assets/settings.md` fit a venture fund: a new fund, a partner hire, a thesis post, a portfolio company. The labs
are strategic investors, so their own moves didn't count. In J6, as Damien, the run added one line to
`## What counts as a reason`:

> The lab, or the parent of the contact's firm, announced a programme, investment or senior hire on deployment
> partners, forward deployed engineers, or AI for government. For GV, Google counts as the firm.

The rerun on Riley and Morgan then wrote their drafts. The Anthropic S-1 stayed `maybe`.

## Sample Riley draft

The Riley draft in `drafts/` matches the run described above. It was written to the warmer-draft rules: a warm open,
the 2026-11-02 news, why that news matters to Riley, the August call, and one ask. It does not restate the 2026-10-15
recap email. That paste lives only in demo `inputs/emails/` for history.
