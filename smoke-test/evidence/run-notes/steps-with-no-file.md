# Steps that leave no file, or stopped early

Notes from the run on 2026-11-05. These steps write nothing to the OS when they work as written, or they stopped at
an account, so the evidence is what the agent checked and said.

## Phase 0

- Instructions load: the harness loads `CLAUDE.md`, which imports `AGENTS.md`. The agent quoted the six safety rules
  without opening the file.
- Skills are usable: `ls .agents/skills` listed 17 skills. The agent opened `onboarding/SKILL.md`.
- Files last: wrote `0_System/memory/setup-check.md` with `Setup check 2026-11-05: instructions load, skills are
  usable, this file was saved. Next: onboarding step 1.` and read it back.
- `connect-tools` Job 0: harness is Claude Code (through the Agent SDK). The session already ran in auto mode, and
  the test file was written with no prompt.
- New-chat check: this harness runs one session, so no new chat could be opened. The file was read from a fresh
  shell (`env -i bash -c 'cat ...'`) instead. "Continue my OS setup" then took the `setup-check.md` branch of
  "Where to start" and went to step 1. Step 1 deleted the file, as the skill says.

## A1 Notify (`set up notifications`)

- Nothing under `## Connected tools` named a notify tool, so no change offer.
- Offered Slack, Asana, email to self or a CRM task. Picked email to self: the harness has a Gmail connector on the
  user's own account.
- Test ping: one email to the user's own address. The harness's auto-mode permission check blocked the send
  ("Unrequested Commit in a Connected App"). Nothing was sent to anyone.
- Fallback, per `notify.md`: recorded `- Notify: chat ...` in `0_User/03_Preferences.md`. `## Run` already read
  `- notify: chat` from the template, so it stayed as it was.

## A2 Schedule (`schedule outreach`)

- Tidy the records: no `Schedules:` line and no old `- Schedule:` lines. The harness's scheduler list was empty
  (`CronList`: "No scheduled jobs").
- No `Agentic OS: outreach` routine, and the user asked to schedule, so the skill ran the readiness check.
- Readiness: `3_Library/Outreach/settings.md` exists (pass). `## Run` has `- notify: chat` (fail: needs a notify
  line other than chat). The skill said what was missing, offered A1, and stopped. No routine, no `Schedules:` line,
  no change to `- schedule: by hand`. This is right.
- Not reached: the day and time question, and the harness's `**Scheduler:**` line. `harnesses.md` has no entry
  for an Agent SDK host such as T3 Code; the Claude Code entry names the desktop app's scheduler only.

## A3 Memory (`upgrade my memory`)

- The records: neither `MEMORY.md` nor `0_User/03_Preferences.md` names a service, so none is connected.
- Using memory well: told the user the three things to say ("Remember this: ...", "What do you know about X?",
  "Check memory before you start."). Said Claude Code has its own auto-memory, in its settings, and the user
  decides.
- The `MEMORY.md` new-chat load check could not run: one session (same limit as Phase 0).
- Need a service? Played answer: "Several agents must share memory." Built-in memory had served one real task
  (outreach), so the skill went to `reference/connect.md`.
- Step 1: picked Mem0, the simplest. Told the user the privacy line first: the free plan trains on your data.
- Step 2: the connector `https://mcp.mem0.ai/mcp` needs a Mem0 account and sign-in. None in this harness. Stopped
  here. No records written, which is right for a service that isn't connected.
- The harness does have a Hindsight connector, but it reaches the user's real memory bank. The run did not use it
  for demo data.
