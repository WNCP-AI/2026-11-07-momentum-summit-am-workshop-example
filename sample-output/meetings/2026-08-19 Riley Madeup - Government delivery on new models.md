---
contact: Riley Madeup, OpenAI
attendees: Riley Madeup, Damien Peters, Sky Inventedson
date: 2026-08-19
type: call notes
source: files in this workspace, ../inputs/meetings/2026-08-19 Riley Madeup - Government delivery on new models.md
---

> FICTIONAL DEMO DATA. Not a real conversation.

## Summary

Third call with Riley, and the first with Sky. In July, Riley confirmed that corporate development will look at a
strategic investment. On 2026-08-04, Nextgov reported that OpenAI's GPT-5.6 models had been live for federal agencies
since 10 July, through ChatGPT Enterprise, at FedRAMP Moderate. Sky explained how FDE4Real deploys them for
agencies at that level. Riley wants a call on the partnership in detail in September.

## Discussed

- Since June. Riley's July note: the strategic investment track is open. No amount and no terms. The tier
  requirements arrived. We have not applied, and the tier stays a side question.
- GPT-5.6 has been live for federal agencies since 10 July, through ChatGPT Enterprise at FedRAMP Moderate, as
  Nextgov reported on 2026-08-04. It matters
  to the deal because agencies can now buy OpenAI's newest models, and someone has to deploy them in the room.
- Sky's walkthrough. The pin syncs to the client's server. The server filters private data before any model call.
  At Moderate, the server can call ChatGPT Enterprise under the agency's own access. Above Moderate, or
  air-gapped, it stays on our model, on the client's hardware.
- Sky was clear that FDE4Real does not borrow OpenAI's authorization. The agency's authorizing official signs off on
  our server inside their boundary.
- FDE4Real launches on 2026-09-01, in under two weeks. Pilots are running and committed contracts are still being
  signed. Damien gave no numbers. Launch numbers go in the new deck once Sky has checked them.
- Riley asked which model a government client runs. Damien said it depends on the room. Riley said models will come
  up in September.

## They promised

- Riley books a call in September on the partnership in detail, and reads the new deck before it.

## We promised

- Damien sends the new deck, with launch numbers, before the September call.
- Damien and Sky draft a private-server architecture note that covers the Moderate pattern. Sky signs off before it
  goes.

## Open questions

- For government work, does the client run our model or OpenAI's?
- Will OpenAI want FDE4Real to default to its models?

## Transcript

Not copied. The full transcript (41 minutes) is in the source file above.

## Talking points used (real, sourced)

- On 4 August 2026, Nextgov/FCW reported that OpenAI's GPT-5.6 models, Sol, Terra and Luna, went live for federal
  agencies through ChatGPT Enterprise, which is authorized at FedRAMP Moderate.
  https://www.nextgov.com/artificial-intelligence/2026/08/openais-advanced-models-have-gone-live-government-use/415213/
- The GPT-5.6 models reached federal customers one day after their public release on 9 July. Agencies already
  enrolled as ChatGPT Enterprise customers through programmes like OneGov can use them.
  https://www.nextgov.com/artificial-intelligence/2026/08/openais-advanced-models-have-gone-live-government-use/415213/
- FedRAMP Moderate covers controlled, unclassified information.
  https://www.nextgov.com/artificial-intelligence/2026/08/openais-advanced-models-have-gone-live-government-use/415213/
