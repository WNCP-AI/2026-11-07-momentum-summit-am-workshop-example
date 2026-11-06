# Smoke test: every OS feature, end to end

> **FICTIONAL DEMO DATA.** The contacts, calls, emails and drafts here come from the invented deal in `../CAST.md`.
> The news items are real and sourced. Nothing here was sent to anyone.

One fresh run on 2026-11-05, from Phase 0, Check the setup, to Phase 3, Better research. It checks each feature against its skill. Every
row passed, was partly checked, or stopped where an account or a permission was needed. No row failed. The run found 8 small skill bugs
and 5 gaps in this folder's README. They are listed under "Failures" below.

## The run

- **Harness:** Claude Code, through the Claude Agent SDK in T3 Code. Model: Claude Opus 5.5 (`claude-opus-5-5`).
- **Workspace:** `/tmp/wnc128-smoke/`, outside the repo, holding a fresh copy of `agentic-os/` from `origin/dev`
  at `333b408` and an `inputs/` folder next to it. The task said to copy `inputs/` into the OS folder. This
  folder's README says to put it next to the OS folder, and the run followed the README.
- **Data:** the step prompts ask the agent to fetch each folder from GitHub. The run copied the same folders from
  the worktree instead, one step at a time, at the step that uses them.
- **Prompts:** typed word for word from `../README.md`, `## Prompts, one step at a time`. That README has no
  prompts for Phase 3, so those used the lines in the What's next table of `outreach-setup`. Answers the README doesn't
  script were played as Damien and are marked "played".
- **News:** built-in web search and fetch. Better research added Firecrawl.
- **Time:** the agent's own time per step, measured from its clock. It leaves out a person reading and typing,
  so a workshop takes much longer.

## Results

| Step | Prompt typed | Pass / Fail / Needs account | Evidence | Time | Notes |
|---|---|---|---|---|---|
| Phase 0. Check the setup | Kickoff prompt from `agentic-os/README.md` | Partly checked | `evidence/run-notes/steps-with-no-file.md` | <1 min | The skill's new-chat check wasn't run: this harness can't open a new chat. The file was read back from a fresh shell instead, which shows the file was kept but not that instructions load in a new chat. Check this in the Grok Bot dry run |
| Phase 1. Memory | None (no question) | Pass | `evidence/0_System/memory/glossary.md` | <1 min | `MEMORY.md` with Me, People, Terms, Projects, Preferences. `people/`, `projects/`, `context/` created. `setup-check.md` deleted |
| Phase 1. About you | The five answers | Pass | `evidence/0_User/01_Overview.md` to `04_Goals.md` | <1 min | `## Me` line written |
| Phase 1. Your company | "Files in this workspace. First get the folder ..." | Pass | `evidence/0_Company/` | <1 min | Six files. `04_Market.md` stays empty: the sources don't cover it. Lab names kept out of the tracked folder (played) |
| Phase 1. Voice | "Files in this workspace. First get the folder ... use these two" | Pass | `evidence/0_User/05_Voice.md` | <1 min | Both emails saved to `3_Library/Emails/` (see `evidence/workspace-files.txt`) |
| Finish | None | Pass | `evidence/0_System/memory/MEMORY.md` | <1 min | `Onboarding:` line removed, `2026-11-05: OS set up` under `## Log` |
| Phase 2. Your project | "set up outreach" | Pass | `evidence/1_Work_Projects/2026.11.05 Outreach/README.md`, `evidence/gitignore-added.txt` | <1 min | Project gitignored before any file went in. Three assets copied |
| Phase 2. Who you write to | "investor outreach" and the Goal line | Pass | `evidence/1_Work_Projects/2026.11.05 Outreach/outreach-settings.md` | <1 min | Every `<...>` filled from `0_Company/`. `### Sales` removed |
| Phase 2. Your contacts | "My contacts are in files ..." and "Skip anyone whose Stage is Passed or Exec ..." | Pass | `## Contacts` in `outreach-settings.md`, `evidence/0_User/03_Preferences.md` | <1 min | CSV read in place, no rows copied. No path in `## Connected tools` |
| Phase 2. Past conversations | "My call notes are in files ... My sent emails are in files ..." | Pass | `evidence/1_Work_Projects/2026.11.05 Outreach/meetings/`, `evidence/run-notes/j4-history.md` | <1 min | 15 notes saved, transcripts left out. History found two overdue promises from the sent emails |
| Phase 2. First drafts | "run outreach on 3 contacts" | Pass | `evidence/0_System/memory/2026-11-05.md`, `evidence/2_Research/News/2026/11/` | 2 min | 12 read, 4 skipped, 3 checked, 0 drafts, 3 maybes. The default reasons don't fit the labs: the case Make it yours covers |
| Phase 2. Make it yours | The README's "not yet: the labs are strategic investors ..." line, then "good enough" | Pass | `evidence/1_Work_Projects/2026.11.05 Outreach/drafts/`, `sleep-log.md` | <1 min | Reason added to settings. Rerun wrote Riley and Morgan. Avery stayed at `maybe` |
| Phase 2. What's next | List shown (no promote line) | Pass | `evidence/1_Work_Projects/2026.11.05 Outreach/README.md`, memory log | <1 min | Status "Working". Promotion moved to Schedule (WNC-138) |
| Phase 3. Notify | "set up notifications" | Needs account | `evidence/0_User/03_Preferences.md`, `evidence/run-notes/steps-with-no-file.md` | <1 min | Email to self picked. The harness's permission check blocked the test send. Fell back to `notify: chat` |
| Phase 3. Schedule | "schedule outreach" | Needs account | `evidence/run-notes/steps-with-no-file.md` | <1 min | Stopped at the readiness check, as the skill says: it needs a notify line other than chat. No routine created |
| Phase 3. Memory | "upgrade my memory" | Needs account | `evidence/run-notes/steps-with-no-file.md` | <1 min | Guidance given. Connect flow reached Mem0's sign-in. No records written |
| Phase 3. Deep voice | "learn my voice from my emails" | Pass | `evidence/0_User/05_Voice.md`, `evidence/run-notes/a4-proof.md` | <1 min | Two types, from 6 and 3 sent emails in `inputs/emails/`. Each has a `Checked:` line after the side-by-side proof |
| Phase 3. Better research | "add better news sources" | Pass | `## News` in `evidence/3_Library/Outreach/settings.md`, `evidence/run-notes/a5-compare.md` | <1 min | Firecrawl compared on Riley and kept. LinkedIn declined (played). Used the harness's existing Firecrawl connector: the free sign-up at the hosted MCP was not tested |

## The WNC-127 fixes

| Check | Result | Evidence |
|---|---|---|
| History reads the sent emails | Pass. It used the 2026-10-15 recap to Riley, and saw that the last email to Morgan was 2026-08-27, so the promised 20 November note was never sent | `evidence/run-notes/j4-history.md` |
| Riley's draft owns the open model-terms promise and doesn't claim it was sent | Pass: "I owe you the model-terms page. It was due on 21 October and it is late. It comes `<date>`." | `evidence/1_Work_Projects/2026.11.05 Outreach/drafts/2026-11-05 Riley Madeup.md` |
| No contact whose Notes say "Do not contact" gets a draft | Pass. The three such rows are all Stage "Exec", which the Your contacts skip line already drops, so this run didn't test the Notes rule on its own | `drafts/` holds Riley and Morgan only |
| News search tries the company's own site first | Not verified. The agent reported going to anthropic.com/news, openai.com/news and gv.com/news first, but the run didn't record the order of its searches, and the saved articles don't show it. It also reported searching the person after the company and the parent, later than the skill's order. See "Run notes" under Failures | `evidence/2_Research/News/2026/11/` (articles only) |
| The Make it yours rerun covers only the contacts with no draft | Pass. First drafts wrote no drafts, so all three were rerun, which made this check trivial | `evidence/0_System/memory/2026-11-05.md` |

## The records each feature leaves

| Record | Expected | Found |
|---|---|---|
| `0_User/` | 01 to 05, `## Connected tools` | All five. Connected tools: contacts, meeting notes, sent emails, notify |
| `0_Company/` | 01 to 06, distilled | All six. Full documents in `3_Library/` |
| Work project | README, settings, draft, sleep log, `drafts/`, `meetings/`, gitignored | All present. In a test `git init` and `git add -A`, only the tracked files were staged: skills, READMEs, `.gitignore` and `0_Company/` |
| `MEMORY.md` pointer lines | One per feature that has one | `## Me` (onboarding), `Active Library processes: 3_Library/Outreach/ ...` (outreach), `- 2026-11-05: OS set up` (log). No `Schedules:` or `Memory service:` line, which is right because neither was created |
| `AGENTS.md` | Nothing added | `diff` against the repo copy: unchanged. Skills and `inputs/` also unchanged |
| Settings lines | `notify`, `schedule`, `Sources on` | `- notify: chat`, `- schedule: by hand`, `- Sources on: built-in web search, firecrawl` |
| What's next promotion | `3_Library/Outreach/settings.md`, `sleep-log.md`, `Drafts/YYYY/MM/`, `Meetings/YYYY/MM/` | All present (`evidence/workspace-files.txt`) |

## Failures

No step failed. Each item below names the skill and the step, says what happened, and says what was expected.

### Skill bugs

1. **`connect-tools`, Notify** (`reference/notify.md` step 5). It says "add `- notify: <tool>`" to `## Run`. The
   settings template already has `- notify: chat`, so following the line as written gives two `notify` lines.
   Expected: "set the `- notify:` line".
2. **`util-files`, What's next** ("Promote to the Library"). It copies the settings, `sleep-log.md` and `contacts.csv`, but
   not `draft.md`. `outreach` says `draft.md` sits next to the settings file. After promotion it falls back to the
   asset, so a draft template the user edited is lost. Expected: copy `draft.md` too.
3. **`util-files` and `outreach-setup`, What's next.** The promoted `settings.md` still says `Saved to: meetings/ in this
   project` under `## History`. The skills resolve the Library path anyway, so nothing breaks, but the line is now
   wrong. Expected: rewrite it to `3_Library/Meetings/YYYY/MM/` on promotion.
4. **`outreach`, First drafts.** A contact with an overdue promise and no `yes` news gets no draft. The report doesn't
   mention the promise either. Riley would have had nothing without the 2 November news. The Goal says "keep
   every promise we made on a call". Expected: list every overdue promise in the report, with or without a draft.
5. **`outreach-news`, Make it yours.** There's no rule for news the contact has already discussed. Anthropic's GSA expansion
   (2026-10-27) matches the new reason, but Avery and Damien talked about it on the 2026-10-28 call. The run
   labelled it `maybe` on judgement. Expected: a line saying news already in the history is `maybe` or `no`.
6. **`outreach-setup`, Who you write to.** The settings file keeps the template's opening note, "The lines below are an example:
   WNCP AI raising for FDE4Real ...", after every section is filled in. Expected: Who you write to removes that paragraph.
7. **`onboarding`, Memory and Finish.** Memory lists the sections of `MEMORY.md` as Me, People, Terms, Projects,
   Preferences. Finish writes under `## Log`, which Memory never creates. Expected: add Log to Memory's list.
8. **`util-schedule` and `onboarding/reference/harnesses.md`, Schedule.** No entry covers an Agent SDK host, such as
   T3 Code. The Claude Code entry names only the desktop app's scheduler. The run stopped before this mattered.
   Expected: one line on hosts that embed Claude Code.

### Gaps in this folder's README

1. **Your contacts.** The skip line "Passed or Exec" drops the default "Committed". On a 10-contact or scheduled run, Jamie
   Testwell (Committed, "Send updates only") would be checked and could get a draft. The line also skips every
   "Do not contact" row by Stage, so the WNC-127 Notes rule never runs on its own.
2. **Phase 3.** There are no prompts or scripted answers: which notify channel, what day and time, whether a
   memory service is needed, which email types, and whether to keep Firecrawl.
3. **Your company.** No answer is scripted for "Is this confidential?" or for the thin topics (market, competitors,
   pricing).
4. **First drafts.** Expect different news from `sample-output/`. This run didn't find the 2026-11-03 Hg item. It found only
   the FT report from 2026-10-23, which Anthropic hadn't confirmed, so Avery got no draft.
5. **Make it yours.** The check "rerun only the contacts with no draft" can't show anything when First drafts writes no drafts, as it
   did here.

### Run notes

1. **`outreach-news`, First drafts, search order.** The agent reported searching the person after the company and the parent
   company. The skill's order puts the person second. The run didn't log its searches, so neither the newsroom-first
   check nor this order can be shown from evidence. The next run should keep a short search log.
2. **`onboarding`, Phase 0.** The new-chat check stays open until a harness that can start a new chat runs it.

### Limits of this harness

1. **New chat.** The Phase 0 new-chat check and the Phase 3, Memory load check need a new chat. This harness runs one session.
2. **Sending.** The auto-mode permission check blocked the Notify test email to the user's own address. A permission
   rule for the Gmail send tool would allow it.
3. **Fetching openai.com.** `openai.com/news` returned 403 to the fetch tool. The search found the OpenAI news through
   CNBC and Fortune instead.
4. **Accounts.** There is no Mem0 account (Phase 3, Memory). No scheduled routine can be created (Schedule, by rule). Firecrawl went
   through an existing connector, not the free sign-up (Better research).

## Drafts compared with `sample-output/`

| Contact | This run | `sample-output/` (2026-11-04) |
|---|---|---|
| Riley Madeup | Draft. Cites the Driscoll hire and owns the late model-terms page with `<date>` | Draft. Cites the Driscoll hire but doesn't mention the page |
| Morgan Fakely | Draft. Cites Google Public Sector's FDE academy and sends the 20 November note promised on 29 October | Draft. Cites the same news |
| Avery Fictional | No draft. Hg item unconfirmed, GSA already discussed: both `maybe` | Draft from the Hg item of 2026-11-03 |

## What's in `evidence/`

Copies of the files the run wrote, at their OS paths, small files only. `workspace-files.txt` lists every file in the
workspace at the end of the run. `run-notes/` holds what the agent showed in the chat for the steps that leave no
file. The 14 other meeting notes, the other saved emails and the transcripts are left out.
