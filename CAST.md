# Cast and plan for the demo data

> **FICTIONAL DEMO DATA.** Every conversation, number and person here is invented for the Momentum Summit workshop,
> except the three lab CEOs, who are named so that it's obvious this is a demo. They appear only in group calls, say
> nothing that could pass for a real position or commitment, and their lines are generic. The events in `## News`
> are real and sourced. Nothing here describes a real deal.

This file is the contract for every demo-data task (WNC-83 to WNC-87, and WNC-118 to WNC-121). Use these names,
roles, dates, news ids and paths exactly.

## The story

WNCP AI (Damien Peters, CEO) is raising a strategic investment of $50M to $150M, about $100M, for its subsidiary
**FDE4Real**. All three big labs are talking to us: Anthropic, OpenAI and Google. Each wants a channel into
corporate and government AI budgets. The facts about FDE4Real are in WNC-86. The headline numbers are $35M ARR
within 4 weeks of launch, and $350M in committed contracts.

FDE4Real launched on Tuesday 2026-09-01. Calls before that date have no ARR: only pilots, the build and contracts
being signed. The $35M ARR figure appears from late September on.

The talks run for six months, from May to the end of October 2026. Each lab starts with a warm intro from a friend
of Damien's and a short first call. The deal builds over the summer and comes to a head in the autumn. Every call
turns on one real, dated news event about the lab. The newest news is left unused, so that at demo time
`outreach-news` finds it live and the draft has something new to cite.

## People

All emails use the reserved domain `example.com`, so nothing can reach a real person.

| Name | Firm | Role | Type | Email | In calls |
|---|---|---|---|---|---|
| Damien Peters | WNCP AI | CEO (the user) | — | damien@example.com | all |
| Sky Inventedson | FDE4Real (WNCP AI) | General Manager, FDE4Real | — | sky@example.com | O0c, G0b and all group calls |
| Avery Fictional | Anthropic | Head of Strategic Partnerships | investor | avery.fictional@example.com | A0a, A0b, A1, A2, A3 |
| Jordan Notreal | Anthology Fund (Anthropic and Menlo) | Partner | investor | jordan.notreal@example.com | A2, A3 |
| Dario Amodei | Anthropic | CEO | investor | dario@example.com | A3 only |
| Riley Madeup | OpenAI | VP, Corporate Development | investor | riley.madeup@example.com | O0a, O0b, O0c, O1, O2 |
| Quinn Pretend | OpenAI Startup Fund | Partner | investor | quinn.pretend@example.com | O2 |
| Sam Altman | OpenAI | CEO | investor | sam@example.com | O2 only |
| Morgan Fakely | GV | General Partner | investor | morgan.fakely@example.com | G0a, G0b, G1, G2, G3 |
| Taylor Imaginary | Google Cloud | Director, Enterprise AI Partnerships | investor | taylor.imaginary@example.com | G1, G2 |
| Sundar Pichai | Google | CEO | investor | sundar@example.com | G2 only |
| Parker Notional | Sample Robotics | Founder and CEO. A founder friend of Damien's and a Claude customer | connector | parker.notional@example.com | none (introduced Avery) |
| Ellis Makebelieve | Dummy Systems | CTO. Damien's former colleague, who once worked with Riley | connector | ellis.makebelieve@example.com | none (introduced Riley) |
| Harper Unreal | Placebo Health | Founder and CEO. A GV portfolio founder Damien knows | connector | harper.unreal@example.com | none (introduced Morgan) |
| Casey Placeholder | Cohere | Head of Strategic Investments | investor | casey.placeholder@example.com | none (cold) |
| Drew Sampleton | Example Ventures | Partner | investor | drew.sampleton@example.com | none (passed) |
| Jamie Testwell | Mock Capital | Principal | investor | jamie.testwell@example.com | none (committed) |

## Calls

Five calls per lab, with a different shape each time. All in 2026. The 8 calls marked "existing" keep their ids,
dates and topics. New ids end in a letter so they sort before the old ones: `A0a` comes before `A1`. The first
letter is the lab.

| Id | Date | Lab | Shape | Attendees | Topic | News |
|---|---|---|---|---|---|---|
| A0a | 2026-05-20 | Anthropic | 1:1, how we met | Avery, Damien | Intro from Parker and a first look | N-A1 |
| O0a | 2026-05-21 | OpenAI | 1:1, how we met | Riley, Damien | Intro from Ellis and a first look | N-O1 |
| G0a | 2026-06-11 | Google | 1:1, how we met | Morgan, Damien | Intro from Harper and a first look | N-G1 |
| O0b | 2026-06-24 | OpenAI | 1:1 | Riley, Damien | Partner route or something bigger | N-O2 |
| A0b | 2026-07-15 | Anthropic | 1:1 | Avery, Damien | Partner fit and pilot proof | N-A2 |
| O0c | 2026-08-19 | OpenAI | 2:1 | Riley, Damien, Sky | Government delivery on new models | N-O3 |
| G0b | 2026-08-26 | Google | 2:1 | Morgan, Damien, Sky | Industry editions and where we fit | N-G2 |
| A1 | 2026-09-16 | Anthropic | 1:1 (existing) | Avery, Damien | FDE4Real as forward-deployed partner | N-A3 |
| O1 | 2026-09-23 | OpenAI | 1:1 (existing) | Riley, Damien | FDE4Real for enterprise and government deployments | N-O4 |
| G1 | 2026-09-30 | Google | 1:2 (existing) | Morgan, Taylor, Damien | GV and Google Cloud interest | N-G3 |
| A2 | 2026-10-07 | Anthropic | 1:2 (existing) | Avery, Jordan, Damien | Strategic investment range and structure | N-A4 |
| O2 | 2026-10-14 | OpenAI | Group (existing) | Sam, Riley, Quinn, Damien, Sky | Leadership call on OpenAI versus rivals | N-O5 |
| G2 | 2026-10-21 | Google | Group (existing) | Sundar, Morgan, Taylor, Damien, Sky | Leadership call on Gemini Enterprise channel | N-G5 |
| A3 | 2026-10-28 | Anthropic | Group (existing) | Dario, Avery, Jordan, Damien, Sky | Leadership call and next steps | N-A5 |
| G3 | 2026-10-29 | Google | 1:1 (existing) | Morgan, Damien | Term sheet timing | N-G4 |

Each call ends with something promised and an open question, so a follow-up has something to build on.

### How we met

- **Anthropic.** Parker Notional runs Sample Robotics, a Claude customer, and knows Avery from a customer council.
  Parker emails an intro on 2026-05-12. Damien thanks Parker on 2026-05-13. A0a is a 20-minute first look.
- **OpenAI.** Ellis Makebelieve worked with Damien years ago and with Riley before that. Ellis emails an intro on
  2026-05-13. Damien thanks Ellis on 2026-05-14. O0a is a 20-minute first look.
- **Google.** Harper Unreal runs Placebo Health, a GV portfolio company, and knows Morgan as a board member. Harper
  emails an intro on 2026-06-02. Damien thanks Harper on 2026-06-03. G0a is a 20-minute first look.

The introducers don't join any call. They're named in the first minute of the how-we-met call.

### What each call takes from its news

The news comes up in the call. Someone names it, and the call says why it matters to the deal.

- **A0a** (N-A1): Anthropic is building services capacity with partners for mid-sized firms. Avery asks whether
  FDE4Real could do the same for larger enterprise and government accounts.
- **A0b** (N-A2): Anthropic's new capital includes scaling partnerships. Avery raises a strategic investment for the
  first time, as a question, not an offer.
- **A1** (N-A3): the Services Track tiers reward certified people and customers in production. Damien says FDE4Real
  aims for the top tier, and that the investment would pay for it.
- **A2** (N-A4): Anthropic is paying to train 10,000 forward deployed engineers. Jordan reads it as proof that
  deployment capacity is scarce, which supports FDE4Real's valuation.
- **A3** (N-A5): the day before, Anthropic cut Claude's price for every level of US government by 40%. Dario's
  lines stay generic. Sky says more agencies buying Claude means more agencies need deployment help.
- **O0a** (N-O1): OpenAI has just launched its own deployment company. Riley asks the core question: is FDE4Real a
  partner or a competitor?
- **O0b** (N-O2): OpenAI now has a Partner Network with tiers. Damien says FDE4Real wants more than a badge, and
  Riley says a strategic investment is a separate track.
- **O0c** (N-O3): the newest OpenAI models are live for federal agencies. Sky explains how FDE4Real deploys them at
  FedRAMP Moderate.
- **O1** (N-O4): OpenAI's government pricing runs to the end of 2028. Riley says that gives a government channel a
  long runway.
- **O2** (N-O5): GPT-6 is out. Sam's lines stay generic. Quinn asks how fast FDE4Real can move clients onto a new
  model, against rivals.
- **G0a** (N-G1): Google Cloud has a new practice with IBM that brings forward deployed engineers. Morgan sees a
  fit and offers to bring in Google Cloud later.
- **G0b** (N-G2): Google now packages Gemini Enterprise by industry, with launch partners. Sky asks whether a
  government edition is coming and whether FDE4Real could launch with it.
- **G1** (N-G3): Google Cloud has paired with a private equity firm to bring AI to its portfolio. Taylor uses it as
  the model for one Google package of GV money and Cloud channel.
- **G2** (N-G5): the day before, Google Public Sector launched Gemini for government services with launch
  partners. Sundar's lines stay generic. Taylor asks whether FDE4Real wants to join as a partner.
- **G3** (N-G4): Accenture is building a 1,000-person forward deployed engineer group for Gemini Enterprise. Morgan
  says GV should move before the channel fills up, so timing matters.

### Changes to the 8 existing calls

The existing calls now follow earlier calls. Each lab task edits its own:

- **A1, O1 and G1 must no longer open as a first call.** Each says "First call with ..." in its Summary today, and
  the opening lines read like a first meeting. Rewrite both. A1 and O1 become the first call about the partnership
  in detail. G1 is the first call with Taylor, but not with Morgan.
- Add the moment where the call's news comes up, in the transcript and in Discussed.
- Put the call's news event first under `## Talking points used (real, sourced)`.
- Keep the date, attendees, topic, promises and open questions. Keep within the word budget.

## News

Real events, each opened and checked on 2026-11-04. Calls and emails cite them by id. A "live" event is dated
after its lab's last call: Anthropic 2026-10-28 (A3), OpenAI 2026-10-14 (O2), Google 2026-10-29 (G3). Leave
live events unused: no call, email or talking point mentions them. At demo time `outreach-news` searches the last
90 days, from about 2026-08-08, finds them on its own, and the draft cites news newer than the last conversation.
The same goes for any other news dated after the lab's last call, in this table or not.

| Id | Date | Lab | Event | URL | Used in |
|---|---|---|---|---|---|
| N-A1 | 2026-05-04 | Anthropic | Anthropic, Blackstone, Hellman & Friedman and Goldman Sachs form a new AI services company to bring Claude to mid-sized firms. Anthropic applied AI engineers work with its team | https://www.anthropic.com/news/enterprise-ai-services-company | A0a; email 2026-05-21 to Avery |
| N-A2 | 2026-05-28 | Anthropic | Anthropic raises a $65B Series H at a $965B post-money valuation. Funds go to research, compute, and scaling products and partnerships | https://www.anthropic.com/news/series-h | A0b |
| N-A3 | 2026-06-03 | Anthropic | Anthropic adds a Services Track to the Claude Partner Network, with Select, Preferred and Global Premier tiers, and a Claude Partner Hub | https://www.anthropic.com/news/services-track-partner-hub | A1 |
| N-A4 | 2026-10-02 | Anthropic | Claude Frontier Academy: $100M to train 10,000 Frontier Deployed Engineers by the end of 2027 | https://www.anthropic.com/news/claude-frontier-academy | A2; email 2026-10-09 to Avery and Jordan |
| N-A5 | 2026-10-27 | Anthropic | Anthropic expands its GSA deal: 40% off Claude Enterprise, Claude for Government and the API for federal, state, local and tribal governments | https://www.anthropic.com/news/expanding-partnership-gsa | A3 |
| N-A6 | 2026-11-03 | Anthropic | Anthropic, which filed for a US IPO on 2026-10-26, plans an Australian retail share offer. It is expected to list on Nasdaq as ANT before Thanksgiving | https://www.reuters.com/business/finance/anthropic-plans-australian-share-offer-ipo-commsec-says-2026-11-03/ | live: leave unused |
| N-O1 | 2026-05-11 | OpenAI | OpenAI launches the OpenAI Deployment Company with more than $4B of initial investment, and agrees to buy Tomoro for its forward deployed engineers | https://openai.com/index/openai-launches-the-deployment-company/ | O0a |
| N-O2 | 2026-06-14 | OpenAI | OpenAI launches the OpenAI Partner Network: $150M, a goal of 300,000 certified consultants by the end of 2026, and Select, Advanced and Elite tiers | https://openai.com/index/introducing-openai-partner-network/ | O0b; email 2026-06-25 to Riley |
| N-O3 | 2026-08-04 | OpenAI | OpenAI's GPT-5.6 models go live for federal agencies through ChatGPT Enterprise, which is authorized at FedRAMP Moderate | https://www.nextgov.com/artificial-intelligence/2026/08/openais-advanced-models-have-gone-live-government-use/415213/ | O0c |
| N-O4 | 2026-09-10 | OpenAI | OpenAI and GSA: $0 licence fees and 50% off usage for federal, state, local and tribal governments, from 2026-10-01 to the end of 2028 | https://openai.com/index/expanding-ai-access-us-government/ | O1; email 2026-09-24 to Riley |
| N-O5 | 2026-10-07 | OpenAI | GPT-6 rolls out globally in ChatGPT, with Intelligent UI | https://openai.com/index/gpt-6-for-everyone/ | O2 |
| N-O6 | 2026-11-02 | OpenAI | OpenAI appoints a former US Secretary of the Army as Senior Counselor for National Security Modernization | https://openai.com/index/dan-driscoll-joins-openai/ | live: leave unused |
| N-G1 | 2026-06-04 | Google | IBM and Google Cloud launch a Google Cloud practice on Gemini Enterprise, with Google Cloud-certified consultants and forward deployed engineers | https://www.googlecloudpresscorner.com/2026-06-04-IBM-and-Google-Cloud-Announce-Strategic-Partnership-to-Scale-AI-with-Human-Expertise-and-AI-Powered-Delivery | G0a |
| N-G2 | 2026-08-25 | Google | Google Cloud launches Gemini Enterprise for Financial Services, in preview, with launch partners and systems integrators | https://www.googlecloudpresscorner.com/2026-08-25-Google-Cloud-Launches-Gemini-Enterprise-for-Financial-Services | G0b; email 2026-08-27 to Morgan |
| N-G3 | 2026-08-27 | Google | Clearlake Capital and Google Cloud partner to bring Google Cloud's full AI stack to Clearlake's portfolio companies | https://www.googlecloudpresscorner.com/2026-08-27-Clearlake-Capital-and-Google-Cloud-Form-Strategic-Partnership-to-Deliver-Full-Stack-Enterprise-AI-Across-Portfolio-Companies | G1 |
| N-G4 | 2026-09-08 | Google | Accenture forms a Gemini Enterprise Business Group with a 1,000-person forward deployed engineer workforce | https://www.googlecloudpresscorner.com/2026-09-08-Accenture-and-Google-Cloud-Deepen-Partnership-with-Formation-of-New-Accenture-Gemini-Enterprise-Business-Group | G3 |
| N-G5 | 2026-10-20 | Google | Google Public Sector launches Gemini for government services, in preview for US federal, state and local governments, with launch partners | https://www.googlecloudpresscorner.com/2026-10-20-Google-Public-Sector-Launches-Gemini-for-Government-Services | G2 |
| N-G6 | 2026-11-04 | Google | Google will invest US$15B in Malaysia in 2027 and 2028, with data center capacity for a new Google Cloud region and AI training for local councils | https://www.googlecloudpresscorner.com/2026-11-04-Google-Announces-Digital-Infrastructure-Expansion-Local-Jobs-Water-Replenishment-and-Clean-Energy-Initiatives-with-US-15-Billion-Malaysia-Investment | live: leave unused |

## Sent emails

Short emails Damien sent between calls. Each lab task writes its own. Save each in `inputs/emails/` as
`YYYY-MM-DD <first To name> - <Subject>.md`, in the same format as the two that are there: the FICTIONAL banner,
then From, To, Date and Subject lines, then the body. Keep each under 200 words. An email with a news id names the
event and says in one line why it matters to the deal.

| Date | To | Subject | News id or none |
|---|---|---|---|
| 2026-05-13 | Parker Notional | Thank you for the intro to Avery | none |
| 2026-05-14 | Ellis Makebelieve | Thanks for connecting me with Riley | none |
| 2026-05-21 | Avery Fictional | Good to meet you, and the services company news | N-A1 |
| 2026-06-03 | Harper Unreal | Thank you for the intro to Morgan | none |
| 2026-06-25 | Riley Madeup | The Partner Network, and what we'd want beyond a tier | N-O2 |
| 2026-08-14 | Drew Sampleton | Thanks for the call (existing) | none |
| 2026-08-27 | Morgan Fakely | Recap, and the question of a government edition | N-G2 |
| 2026-09-24 | Riley Madeup | Recap, and the government pricing window to 2028 | N-O4 |
| 2026-10-01 | Jamie Testwell | FDE4Real investor update (existing) | none |
| 2026-10-09 | Avery Fictional, Jordan Notreal | Frontier Academy, and engineers we could nominate | N-A4 |
| 2026-10-15 | Riley Madeup, Quinn Pretend | Recap of the leadership call, and model terms timing | none |

## Word budget

A $20 plan has to read every meeting, so total meeting words stay under about 50,000. The 8 existing calls hold
28,661 words today. "How we met" calls run 15 to 25 minutes. Other new calls run 30 to 45 minutes. Edits to an
existing call add at most 100 words.

| Lab | Existing calls (words now) | New calls (most words each) | Most words for the lab |
|---|---|---|---|
| Anthropic | A1, A2, A3 (10,512) | A0a 2,000; A0b 3,500 | 16,400 |
| OpenAI | O1, O2 (6,525) | O0a 2,000; O0b 3,500; O0c 3,500 | 15,800 |
| Google | G1, G2, G3 (11,624) | G0a 2,000; G0b 3,500 | 17,500 |
| All | 28,661 | 20,000 | 49,700 |

Count with `wc -w` on each meeting file. Emails don't count toward the budget.

## Contact rows

`inputs/contacts.csv` has these columns, matching `## Contacts` in the outreach settings:
`Name, Firm, Role, Type, Email, Stage, Last touch, Notes`.

- **Stage:** Warm (Avery, Riley, Morgan), Active (Jordan, Quinn, Taylor), Exec (the three CEOs), Cold (Casey),
  Passed (Drew), Committed (Jamie).
- **Last touch:** the date of that person's latest call or email in this plan. Casey: 2026-08-12. Drew: 2026-08-14,
  the thank-you email after the 2026-08-12 call. Jamie: 2026-10-01, the investor update.
- **Notes:** one line, for example "Deal lead. Wants the pilot list before the term sheet."

Damien and Sky aren't rows: they're on our side. The three connectors aren't rows either: they're not in the
outreach pipeline.

## Files and which step uses them

The dry run starts from a fresh copy of the OS. Damien copies `inputs/` into it and names each folder when a step asks.

```
workshop-demo-data/
  README.md                      FICTIONAL banner, what's here, and which step uses each input (WNC-86)
  CAST.md                        this file
  inputs/                        what a user would bring
    company/                     → onboarding step 3, Company (WNC-86)
    emails/                      → onboarding step 4, Voice, light (WNC-86; lab emails from WNC-119, 120, 121)
    contacts.csv                 → outreach-setup J3, Contacts: the contact list source (WNC-87)
    meetings/                    → outreach-setup J4, Past conversations: the meeting notes source (WNC-83, 84, 85;
                                   new calls from WNC-119, 120, 121)
```

The example repo is checkpoint 1 from the dry run (WNC-100). It isn't kept here.

## Meeting file format

These are the raw notes a user brings, not the OS's own summaries. They sit flat in `inputs/meetings/`.
`outreach-history` reads them in outreach-setup J4 and saves its own copy to the project's `meetings/`.

Save each call once, named after the lab's deal lead (Avery, Riley or Morgan):
`YYYY-MM-DD <Lead name> - <topic, 3 to 6 words>.md`. This matches the names `outreach-history` saves. List everyone
on the call in `attendees:`, because `outreach-history` also matches on that line.

```
---
contact: <lead name>, <firm>
attendees: <every name on the call, comma-separated>
date: YYYY-MM-DD
type: call notes
source: demo data (fictional)
---

> FICTIONAL DEMO DATA. Not a real conversation.

## Summary
## Discussed
## They promised
## We promised
## Open questions
## Transcript   (the full call, timestamps, `Speaker: line`. Length: see `## Word budget`)
## Talking points used (real, sourced)   (2 to 4 bullets of real public facts about the lab, each with a URL.
                                          The call's news event from `## Calls` comes first)
```

## Rules

- Invented people get obviously fake names, as listed above. Don't add new people. The only additions allowed are
  the three connectors already in `## People`: Parker Notional, Ellis Makebelieve and Harper Unreal.
- The real CEOs: group calls only, a few generic lines each, nothing that sounds like a real company position or a
  real commitment.
- Talking points about the labs are real and sourced: public announcements, programmes or products, each with a
  URL. Everything about the deal is invented. Never invent a news event, a date or a URL.
- Every call uses its news event from `## Calls`, and only news dated before the call.
- Each lab's `live: leave unused` events are dated after that lab's last call. Never use a live event, or any news
  dated after the lab's last call: Anthropic 2026-10-28, OpenAI 2026-10-14, Google 2026-10-29.
- The transcript is the full call, with timestamps. The 8 existing calls run 30 to 60 minutes. New calls follow
  `## Word budget`. Keep Summary, Discussed, promises and open
  questions in line with it. Side details and jokes can live in the transcript so a later follow-up has something
  to pull.
- No real email addresses, phone numbers or private details.
