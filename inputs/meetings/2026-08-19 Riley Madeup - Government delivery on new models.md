---
contact: Riley Madeup, OpenAI
attendees: Riley Madeup, Damien Peters, Sky Inventedson
date: 2026-08-19
type: call notes
source: demo data (fictional)
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

Full call, 41 minutes. Timestamps from the recording.

(00:00:06) Riley Madeup: Damien. And you must be Sky.
(00:00:09) Sky Inventedson: I must be. Hi, Riley. I'm in Denver. If the line drops, it's the office wifi, not the product.
(00:00:16) Damien Peters: Sky runs FDE4Real day to day. I promised in June I'd bring them for the government side. I also promised Sky would correct my adjectives.
(00:00:26) Sky Inventedson: I've already found two in the deck draft. We'll get there.
(00:00:31) Riley Madeup: Good. Before Sky starts, the door. I said I'd tell you by the end of July. I sent the note on the 30th. Corp dev will look at a strategic investment. That's all it says. No amount, no structure, no timeline I'd sign.
(00:00:48) Damien Peters: I read it three times looking for "let's stay close." It wasn't there.
(00:00:53) Riley Madeup: I don't write that. The tier requirements reached you too?
(00:00:57) Damien Peters: They did. We haven't applied. We'll decide after this track goes somewhere or doesn't. It's a side question now.
(00:01:05) Riley Madeup: Fine by me. Partnerships won't be offended. They have a lot of applications. So. Why I wanted Sky. Nextgov ran it on the fourth: our GPT-5.6 models have been live for federal agencies since July. ChatGPT Enterprise, FedRAMP Moderate. Agencies already on ChatGPT Enterprise can use them now.
(00:01:24) Sky Inventedson: Sol, Terra and Luna. A day after the public release, from what I read.
(00:01:29) Riley Madeup: That's right. Here's my question. An agency can buy the model. Who puts it to work in the room? That's where I think you come in, and I want to know if I'm wrong.
(00:01:40) Sky Inventedson: You're not wrong. You might be early. Can I walk it through, and you stop me?
(00:01:45) Riley Madeup: Please.
(00:01:47) Sky Inventedson: Start with the pin. The engineer wears it into meetings the agency already has. It syncs to our server, and our server is inside the agency's boundary, on their hardware or their cloud tenancy. Nothing goes from the pin to a public service. That's a hard rule.
(00:02:06) Riley Madeup: Then where does the model call come from?
(00:02:09) Sky Inventedson: The server. After it filters. Names, case numbers, anything the agency marks as private, out first. Then the server decides where to send the rest. That's where Moderate comes in.
(00:02:22) Riley Madeup: Go on.
(00:02:24) Sky Inventedson: Moderate covers controlled unclassified work. If the agency already uses ChatGPT Enterprise at Moderate, our server can call it under the agency's own access. Their contract, their account. We're a client of their setup. We don't carry a separate pipe.
(00:02:42) Damien Peters: That's the sentence I'd have got wrong.
(00:02:45) Sky Inventedson: It's the one that matters. We don't borrow your authorization, Riley. Our server isn't on any marketplace. It runs inside their boundary, and their authorizing official signs off on it. If an outline says "FDE4Real is FedRAMP authorized," I'll strike it.
(00:03:02) Riley Madeup: I'd strike it too. What happens above Moderate?
(00:03:06) Sky Inventedson: Then the server doesn't call out. It stays on our model, on their hardware. Air-gapped sites never had a path to begin with. The city pilot works that way, and it's smaller dollars. But it's the proof that we can go dark.
(00:03:22) Riley Madeup: So for one agency, two answers. Moderate work could run on our newest models. Higher work stays on yours.
(00:03:30) Sky Inventedson: In the same building, sometimes. Same pin, same server, different routing. The routing rule is the agency's, not ours.
(00:03:38) Riley Madeup: That's why the news matters to me. Agencies can buy GPT-5.6 today. Most of them don't have a team that knows how to put it into a workflow. If you're that team, our models get used. If you're not, they sit in a portal.
(00:03:54) Damien Peters: And for us, it means the agencies we serve can reach your newest models without waiting for us to build a separate path. That's a better offer for the client. I'm not going to pretend it isn't.

(00:07:12) Riley Madeup: Stop me if this is a Sky question. How fast does a new model reach a site?
(00:07:18) Sky Inventedson: It's a Sky question. The agency turns it on first. Then we run the recording check on that site's own sample. Every summary against the recording. If the new model does worse on their meetings, we don't switch, and we say why.
(00:07:36) Riley Madeup: You check our model against your recordings?
(00:07:39) Sky Inventedson: We check any model against the recordings. The near-zero number Damien uses is ours, on our model. It is not a claim about anyone else's. When the server calls yours, we measure that too, and it's a separate number.
(00:07:54) Damien Peters: Sky will make me write that in the first line of everything.
(00:07:58) Sky Inventedson: I already have.

(00:12:30) Riley Madeup: Which model does a government client run, then? Not the routing. The default.
(00:12:36) Damien Peters: It depends on the room. If the agency is already on ChatGPT Enterprise at Moderate, that's a natural default for that work. If it's higher, it's ours. I don't want to answer for every agency on a call.
(00:12:50) Riley Madeup: I'm not asking you to. I'm telling you someone in September will ask. If corp dev engages, models come up. I said that in June.
(00:12:59) Damien Peters: You did. I'd rather have the question on paper than in a hallway.
(00:13:04) Riley Madeup: Then let's have a proper call in September. The partnership in detail. Not a walkthrough. What we'd each want.
(00:13:12) Damien Peters: Yes. And before that, I'll send you the new deck.
(00:13:16) Riley Madeup: With numbers? You launch on the first.
(00:13:18) Damien Peters: On the first of September. There's no revenue yet. The pilots are running and the contracts are still being signed. I'll send numbers once, after launch.
(00:13:26) Sky Inventedson: And I check them before they go. If one of them is big, I want it defined before Damien says it out loud.
(00:13:34) Riley Madeup: Then I'll wait for the deck. I'll read it before the call. Maybe twice.
(00:13:39) Damien Peters: Twice would be a record.

(00:18:44) Riley Madeup: The thing I'd want on paper. Not the deck. How the server sits in an agency. The thing Sky just said, with boxes.
(00:18:52) Sky Inventedson: An architecture note. We'll write it. Damien drafts, I mark it up. It covers the Moderate pattern and the air-gapped one.
(00:19:00) Riley Madeup: When?
(00:19:02) Sky Inventedson: When it's right. I'm not giving you a date I'll miss. Damien will give you one in September.
(00:19:08) Damien Peters: I will. Sky's red pen is slow and it's never wrong.
(00:19:12) Riley Madeup: I'd rather wait for that than read a fast one.

(00:24:20) Riley Madeup: One last thing before Sky leaves. Who's on site? I get pitched marketplaces with a hardware accessory.
(00:24:27) Sky Inventedson: Ours. Our engineers, plus a few domain specialists. Not a marketplace. If an outline says "network of experts," I'll replace it.
(00:24:36) Riley Madeup: I'll avoid the phrase. Thanks, Sky. That was the long version I wanted.
(00:24:41) Sky Inventedson: It was the medium version. The long one is in the note. Bye, Riley.
(00:24:46) Riley Madeup: Bye. Damien, promises.
(00:24:49) Damien Peters: You book a September call on the partnership in detail. You read the deck first. I send the deck with launch numbers before that call. Sky and I write the architecture note, and Sky signs off before it goes. Open on your side: will OpenAI want us to default to its models? Open on mine: for government, which model does the client run?
(00:25:12) Riley Madeup: That's the list. I'll send dates. Bye.
(00:25:15) Damien Peters: Bye, Riley.

(00:33:02) Damien Peters: Note for Sky, even though you were here. Riley got corp dev to engage, note of 30 July, no amount. Tier requirements came, we haven't applied. GPT-5.6 is live for federal agencies at Moderate, since July, per Nextgov on the fourth. Riley thinks we're the team that puts it to work. Your line: we don't borrow their authorization. Their official signs off on our server. Moderate can call ChatGPT Enterprise under the agency's access. Higher stays on ours. Near zero is our model only. Riley wants the September call on the partnership in detail and will read the deck first. We launch on the first. We owe the deck with launch numbers, checked, and the architecture note. No date given for the note yet. Models will come up. End note.
(00:34:10) [Room tone. Recording ends 00:41:22.]

## Talking points used (real, sourced)

- On 4 August 2026, Nextgov/FCW reported that OpenAI's GPT-5.6 models, Sol, Terra and Luna, went live for federal
  agencies through ChatGPT Enterprise, which is authorized at FedRAMP Moderate.
  https://www.nextgov.com/artificial-intelligence/2026/08/openais-advanced-models-have-gone-live-government-use/415213/
- The GPT-5.6 models reached federal customers one day after their public release on 9 July. Agencies already
  enrolled as ChatGPT Enterprise customers through programmes like OneGov can use them.
  https://www.nextgov.com/artificial-intelligence/2026/08/openais-advanced-models-have-gone-live-government-use/415213/
- FedRAMP Moderate covers controlled, unclassified information.
  https://www.nextgov.com/artificial-intelligence/2026/08/openais-advanced-models-have-gone-live-government-use/415213/
