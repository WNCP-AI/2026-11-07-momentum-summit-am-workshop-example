# Outreach settings

Filled in by `outreach-setup`. Edit any line yourself, or say "change my outreach settings".

The lines below are an example: WNCP AI raising for FDE4Real, in investor mode. `outreach-setup` replaces each
section with yours before the first run. The `<...>` in the reasons and drafts come from your company files. The
line under each heading says what goes there.

## Mode

> investor, sales or both. With both, each contact row has a Type column.

- Mode: investor

## Goal

> One or two sentences per mode. Every draft serves this.

- Investor: Keep Anthropic, OpenAI and Google warm until one leads the FDE4Real round, and keep every promise we made
  on a call.

## Contacts

> Where the list lives, how to read it, the columns, who to skip and who goes first.

- Source: files in this workspace, `../inputs/contacts.csv`
- Read with: the agent's own file access, read-only
- Columns: Name, Firm, Role, Type, Email, Stage, Last touch, Notes
- Skip: Stage is "Passed" or "Exec"
- Priority: Stage "Warm" first, then the oldest Last touch

## History

> Where past conversations and sent emails live, how to read them, and the fallback. `Emails:` is optional.

- Source: files in this workspace, `../inputs/meetings/`
- Emails: files in this workspace, `../inputs/emails/`
- Read with: the agent's own file access, read-only
- Saved to: `meetings/` in this project, as `YYYY-MM-DD <Contact> - <topic>.md`
- Fallback: the user pastes notes into the chat

## News

> Which sources are on, and what to do with weak results.

- Sources on: built-in web search
  > Allowed: built-in web search (default), firecrawl, linkedin. An upgrade in `outreach-news` adds one.
- LinkedIn limit: 10 profiles per run
- Window: 90 days
- Weak results: label it maybe and write no draft. List them for the user
- Skip: awards lists, generic industry news, and people with a similar name

## What counts as a reason

> Write a draft only for a dated item, about this person or their company, that matches a line below.

### Investor

- The firm raised a new fund
- The firm hired a partner or principal
- The person published a thesis post or spoke about a theme close to forward deployed engineering, or AI deployment
  in enterprise and government
- A portfolio company raised, launched or was acquired
- The lab, or the parent of the contact's firm, announced a programme, investment or senior hire on deployment
  partners, forward deployed engineers, or AI for government. For GV, Google counts as the firm.

## Drafts

> What each draft asks for, how long it is, and the sign-off.

### Investor

- Ask: a 20-minute call about the FDE4Real strategic round, only after the news line and the past-conversation line
- Length: under 120 words
- Sign-off: first name only
- No deck attached unless they asked for it

## Run

> How the user hears about a run, when it runs, and how many contacts it checks.

- notify: chat
- schedule: by hand
- limit: 10 contacts per run
- Sleep after a draft: 1 month
