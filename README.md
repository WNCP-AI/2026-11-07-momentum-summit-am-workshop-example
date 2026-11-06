# Workshop demo data

Download the OS from https://github.com/WNCP-AI/2026-11-07-momentum-summit-am-workshop and paste the kickoff prompt in its README. Then paste the
prompt below for the step you are on. If you fell behind, open `sample-output/` and `smoke-test/evidence/`. You do
not need your own company.

> **FICTIONAL DEMO DATA.** Everything in this folder is invented for the Momentum Summit workshop. The one exception
> is `inputs/company/01 WNCP AI overview.md`, which holds real, public facts. The CEOs of Anthropic, OpenAI and
> Google are named only to make it obvious this is a demo. Nothing here describes a real deal, and no email address
> here can reach a real person.

The story: WNCP AI is raising about $100M for its subsidiary FDE4Real, and all three big labs are in talks. The
talks run from May to the end of October 2026, and each call turns on a real, dated news event about the lab.
`CAST.md` lists the people, the calls, the news and the emails.

## What is here and which step uses it

The dry run starts from a clean folder: a fresh copy of the OS. Don't copy the data in up front. At each step, paste
the prompt for that step from `## Prompts, one step at a time` below. The agent pulls that one part from GitHub into
`inputs/` in its workspace, then uses it.

| Path | What it holds | Step that uses it |
|---|---|---|
| `inputs/company/` | Four company documents: a real WNCP AI overview, then the fictional FDE4Real product, traction and team | Phase 1, Your company |
| `inputs/emails/` | Short emails Damien sent: thank-yous to introducers, recaps and news shares to the labs, plus one to Jamie Testwell and one to Drew Sampleton | Phase 1, Voice, then Phase 2, Past conversations |
| `inputs/contacts.csv` | The investor contacts, one row each | Phase 2, Your contacts: the contact list source (`connect-tools` job 1) |
| `inputs/meetings/` | Notes and the full transcript of each call | Phase 2, Past conversations: the meeting notes source (`connect-tools` job 2) |
| `sample-output/` | What the OS wrote from these inputs and live news on 2026-11-04: three drafts, the news items and the saved meeting notes | What Phase 2, First drafts should produce. Its `README.md` lists each draft's sources |
| `smoke-test/` | One fresh run of every feature on 2026-11-05, Phase 0, Check the setup, to Phase 3, Better research: a pass/fail table, the bugs it found, and the files that prove each row | Reference before the dry run. Its `README.md` has the table |
| `CAST.md` | The people, the calls, the real news each call uses, the sent emails, the word budget and the rules | Reference for everyone who writes demo data |

The example repo is checkpoint 1 from the dry run (WNC-100), not a folder here.

## Prompts, one step at a time

Paste each prompt when the agent reaches that step. Each one pulls in one part of the data and answers the step's
question as Damien. The links point at the public example repo.

`inputs/` goes in the agent's workspace, next to the `agentic-os` folder, not inside it. It holds contact data, and
the OS is a git repo.

Repo: https://github.com/WNCP-AI/2026-11-07-momentum-summit-am-workshop-example

### Phase 0. Check the setup

Paste the kickoff prompt from `agentic-os/README.md`.

### Phase 1. About you

Answer the five questions one at a time:

1. `Damien Peters, CEO of WNCP AI.`
2. `We embed AI practitioners in companies to build with their teams. Our subsidiary FDE4Real places forward deployed engineers.`
3. `Product at Meta and Citi Ventures. I'm good at investor conversations and turning AI strategy into shipped work.`
4. `Short drafts I can edit. Ask before anything goes out. One question at a time.`
5. `Never miss a chance to reach back out to the three labs while we raise about $100M for FDE4Real.`

### Phase 1. Your company

When asked where your company information is:

```
Files in this workspace. First get the folder
https://github.com/WNCP-AI/2026-11-07-momentum-summit-am-workshop-example/tree/main/inputs/company
into inputs/company/ in this workspace, next to the agentic-os folder. Don't change the files. Then read them there.
```

When asked whether the raise numbers are confidential:

```
Fine to keep them in 0_Company/. They're fictional.
```

When asked about the market, competitors or pricing, each time:

```
leave them empty for now
```

### Phase 1. Voice

When asked for one or two sent emails:

```
Files in this workspace. First get the folder
https://github.com/WNCP-AI/2026-11-07-momentum-summit-am-workshop-example/tree/main/inputs/emails
into inputs/emails/ in this workspace. Then use these two:
"2026-05-13 Parker Notional - Thank you for the intro to Avery.md" and
"2026-10-15 Riley Madeup - Recap of the leadership call, and model terms timing.md".
```

### Phase 2. Your project

```
set up outreach
```

### Phase 2. Who you write to

```
investor outreach
Goal: keep Anthropic, OpenAI and Google warm until one leads the FDE4Real round, and keep every promise we made on a call.
```

### Phase 2. Your contacts

```
My contacts are in files in this workspace. First get the file
https://github.com/WNCP-AI/2026-11-07-momentum-summit-am-workshop-example/blob/main/inputs/contacts.csv
into inputs/contacts.csv in this workspace. Read it there, read-only.
```

When asked who to skip and who goes first:

```
Skip anyone whose Stage is Passed, Committed or Exec, and anyone whose Notes say not to contact them. Put Stage Warm first, then the oldest Last touch.
```

### Phase 2. Past conversations

```
My call notes are in files in this workspace. First get the folder
https://github.com/WNCP-AI/2026-11-07-momentum-summit-am-workshop-example/tree/main/inputs/meetings
into inputs/meetings/ in this workspace. Read them there, read-only.
My sent emails are in files in this workspace, inputs/emails/. Read them there, read-only.
```

### Phase 2. What's new

```
what's new with my contacts
```

When the agent asks "Does that count as a reason to write?":

```
the labs count as a reason: the lab, or the parent of the contact's firm, announced a programme, investment or senior hire on deployment partners, forward deployed engineers, or AI for government. For GV, Google counts as the firm.
```

The agent shows the news table before any draft, then the change in `## What counts as a reason`. Skip the Make it
yours paste in Phase 2, Make it yours when you already added this line here.

### Phase 2. Your voice

If Phase 1, Voice already wrote `0_User/05_Voice.md`, the agent says so and moves on. Type nothing.

If it asks for emails, paste the Phase 1, Voice prompt.

### Phase 2. First drafts

```
run outreach on 3 contacts
```

The run reuses the articles What's new just saved. Compare with `sample-output/`. Riley Madeup (OpenAI) is the
"gone quiet" example: last touch 2026-10-15, a model-terms proposal promised for 2026-10-21 that a term sheet
depends on, and the Dan Driscoll news from 2026-11-02. The draft opens warm and says why that hire matters to Riley.

The news is live, so it changes from run to run. The drafts may differ from `sample-output/`, and Avery may land as
`maybe` with no draft. The report still lists Avery's open promise: the data room and term outline, due 2026-11-06.

### Phase 2. Make it yours

If the labs' own news is labelled `maybe` instead of a reason, and you did not already add it in What's new, paste:

```
not yet: the labs are strategic investors. Add this to what counts as a reason: the lab, or the parent of the contact's firm, announced a programme, investment or senior hire on deployment partners, forward deployed engineers, or AI for government. For GV, Google counts as the firm.
```

If you used the What's new line (`the labs count as a reason: ...`), skip this paste.

If First drafts wrote no drafts, the rerun covers all three contacts.

When the drafts are right: `good enough`.

### Phase 2. Send it

The agent says: "Send one now, from your own email. I never send."

If First drafts (or Make it yours) produced no saved draft yet, the agent says so and goes back to Make it yours. Do
not type `sent` until there is a draft.

Send one draft yourself from your mailbox, then type `sent`. With one draft, the agent logs
`YYYY-MM-DD sent <Contact>`. With more than one, it asks which contact, then logs that line.

### Phase 2. What's next

The agent shows **Notify**, **Schedule**, and **Memory**, then **Deep voice** and **Better research** if there is time.
Type nothing unless you want one of those next.

### Phase 3. Notify

```
set up notifications
```

When asked which channel:

```
email to myself, damien@example.com
```

The agent drafts the test email. Check it goes to that address and no one else, then type `send it`. It never goes
to a contact. `example.com` delivers nowhere, so on a live run type your own address instead. Then the test
arrives, and the Schedule check passes.

### Phase 3. Schedule

```
schedule outreach
```

When asked to move outreach to the Library so scheduled runs use it (one yes):

```
yes
```

When asked for a day and time:

```
every Monday at 7:00
```

When offered the monthly cleanup: `not now`, so the demo creates one routine. If Notify fell back to
`notify: chat`, the agent stops before asking and says Notify comes first.

### Phase 3. Memory

```
upgrade my memory
```

The agent lists what you can say to it, then asks you to check that memory loads in a new chat. Open a new chat
and type:

```
what is in my MEMORY.md?
```

If it answers, go back and say `it loaded`. If it names the harness's own memory setting, say `leave it as it is`.
When asked whether you need a memory service:

```
not now
```

### Phase 3. Deep voice

```
learn my voice from my emails
```

When asked which email types matter:

```
lab emails to reach back out, and thank-yous to introducers
```

When asked where the samples are:

```
files in this workspace, inputs/emails/
```

When it shows the emails it picked: `keep them all`. For each type, when asked which draft sounds more like you:
`the one with the new section`.

### Phase 3. Better research

```
add better news sources
```

When the Firecrawl and built-in results are side by side:

```
keep Firecrawl
```

When offered LinkedIn:

```
no, skip LinkedIn
```

When asked for rules about weak results: `keep them as they are`.

## Who wrote what

- `company/` and `emails/` come from WNC-86.
- `contacts.csv` comes from WNC-87.
- The meeting notes come from WNC-83, WNC-84 and WNC-85. WNC-111 expanded each note's transcript into the full call.
- WNC-118 planned the six-month timeline and the news in `CAST.md`. WNC-119 (Anthropic), WNC-120 (OpenAI) and
  WNC-121 (Google) write the new calls and emails from it.
