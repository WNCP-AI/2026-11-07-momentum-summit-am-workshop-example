---
contact: Morgan Fakely, GV
attendees: Sundar Pichai, Morgan Fakely, Taylor Imaginary, Damien Peters, Sky Inventedson
date: 2026-10-21
type: call notes
source: demo data (fictional)
---

> FICTIONAL DEMO DATA. Not a real conversation.

## Summary

Leadership call that Morgan set up after the September call. Sundar opened and left the detail to Morgan and Taylor.
Sky walked through deployments and the private-data filter. Taylor laid out a Gemini Enterprise channel for
corporate and government clients. Morgan said GV could take up to $60M of the round.

## Discussed

- Follow-ups from 30 September: Taylor sent the Gemini Enterprise partner onboarding pack. Damien opened the data
  room and sent the pilot list and the brief on running Gemini on the FDE4Real server. Our near 0% hallucination
  rate is measured on our own model, not on Gemini, so Taylor asked for a test.
- Sky showed how the wearable syncs to the client's server and filters private data before anything is stored.
- Taylor proposed listing FDE4Real in Gemini Enterprise, with Gemini as a model choice on the server.
- Gemini for government services launched the day before, in preview, with launch partners. It answers Sky's
  August question. Taylor asked if FDE4Real wants to join as a partner.
- Government: Taylor wants FDE4Real in air-gapped sites that run Google Distributed Cloud.
- Morgan reviewed the pilot list from the data room. GV could take up to $60M of the $100M round.
- Damien asked for one Google partner across investment and channel.

## They promised

- Taylor: draft a co-sell outline for the Gemini Enterprise channel by early November.
- Morgan: take FDE4Real to the GV partner meeting next week.

## We promised

- Sky: send deployment data for the top 10 clients and an air-gapped test plan.
- Damien: send the cap table and the round's current terms to Morgan.

## Open questions

- Does the Google Cloud co-sell deal sit inside the term sheet or beside it?
- Does Gemini on the FDE4Real server keep the near 0% hallucination rate? The air-gapped test plan will include it.

## Transcript

Full call, 54 minutes. Timestamps from the recording.

(00:00:05) Morgan Fakely: Everyone's on except Sundar, who is joining for the open and then leaving. Damien, Sky, you met Taylor. Taylor, Sky Inventedson runs FDE4Real. They own the deployments. Please don't make them repeat the whole September call.
(00:00:22) Sky Inventedson: I won't repeat it if nobody asks me to repeat it. Hi, Taylor.
(00:00:28) Taylor Imaginary: Hi. I sent the partner pack. Damien marked it up, which I asked for, and then I was briefly sad, which I deserved.
(00:00:37) Damien Peters: The markup was Sky's. I just forwarded it with the subject line "as promised," and Morgan wrote back "the calculator agrees," which I think was a joke.
(00:00:48) Morgan Fakely: It was not a joke. The IRR on the pilot sizes is boring in a way I like. Sundar's in the waiting room. I'm letting them in.
(00:01:02) Sundar Pichai: Thanks for making the time, everyone. Good to see you.
(00:01:08) Damien Peters: Thank you. Sky will show you what the teams do on site. I'll stay out of the way for that part.
(00:01:16) Sundar Pichai: I'd like that. I don't need the financing. I want the work.
(00:01:22) Sky Inventedson: Short version. An engineer wears a pin into meetings they were already having. The pin syncs to a server the client runs. The server strips private data before it stores a word. What's left becomes a knowledge base the team can argue with. Week two, they pick one use case, not a transformation program. If I say "synergy" at any point, you can hang up.
(00:01:52) Sundar Pichai: I like hearing how teams work with customers on the ground.
(00:01:58) Sky Inventedson: That's the whole product. The ground is messy. Northline's program lead asked the pin, on day three, if it was recording. It doesn't talk back, which is lucky, because the honest answer is yes, if it's on. We put that sentence in the statement of work after, not before. I'm not proud of the order.
(00:02:22) Damien Peters: I am a little proud. We wrote it down the same day.
(00:02:27) Taylor Imaginary: The pack I sent assumes a listing. Sky, your markup said you're a deployment, not a tile in a catalog. I agree. What I want to propose, and I'm proposing it to this room, not announcing it, is listing FDE4Real in Gemini Enterprise and offering Gemini as a model choice on your server.
(00:02:52) Sky Inventedson: Clients can pick it. Our model stays the default. The near-zero hallucination rate is measured on our model, against the recording, not on Gemini. Damien already told you that. I'm telling you again because it's the sentence that gets edited out of decks.
(00:03:12) Taylor Imaginary: I didn't edit it out. I do want a test. If Gemini sits on your server, what happens to the rate. I don't need the answer today. I need a plan.
(00:03:24) Sky Inventedson: You'll get a plan. Air-gapped, and also a normal client path, so we don't pretend a bunker and a hospital are the same machine.
(00:03:34) Sundar Pichai: I'll leave the details with Morgan and Taylor. Thank you for the time. It was good to meet the team.
(00:03:42) Damien Peters: Thank you. We'll follow up with them, not with your office.
(00:03:48) Sundar Pichai: That's the right path. Bye.
(00:03:52) Morgan Fakely: He's gone. Sky, keep going. The filter is the part I still want to see with my eyes, not in a paragraph.
(00:04:02) Sky Inventedson: Sharing the diagram Damien sent Taylor. Top box is the pin. It holds audio until it can see the client server. It does not have a consumer-cloud account. If it can't reach the server, it holds or it dumps, and the dump is the client's policy, written down, not a default I hid in a setting.
(00:04:28) Taylor Imaginary: Dump meaning delete?
(00:04:31) Sky Inventedson: Delete on the device. Some clients want a sealed copy in their evidence locker instead. Red Kite Civic wanted the locker. Harborlight Health wanted the delete. Both are in the pilot list you already have. I won't mix them up to make the story cleaner.
(00:04:50) Damien Peters: The one-pager said this. Sky is ruder and more correct.
(00:04:56) Sky Inventedson: Middle box is the filter. It runs on the client server before storage and before any model call. Names, account numbers, the obvious stuff, plus a client list of "never keep this." Harborlight added a list. It was long. We didn't argue. Bottom box is the knowledge base, and only then a model call if the use case needs one.
(00:05:22) Morgan Fakely: So a model outage doesn't delete the week.
(00:05:26) Sky Inventedson: Correct. The week is already notes. The model is a reader. If Gemini is the reader that day, Gemini is the reader. If our model is, ours is. The capture doesn't care. That's why I can offer the choice without rewriting the pin.
(00:05:44) Taylor Imaginary: Government is the bigger prize for me. Air-gapped sites that run Google Distributed Cloud. I need your pin and your server to live there without phoning home to make a point.
(00:06:00) Damien Peters: We're cleared for top-secret work. That fits the rooms you're describing. The papers are in the data room Morgan already has. I still won't recite stamp numbers from memory.
(00:06:14) Sky Inventedson: And "cleared" is not "every building on earth." Red Kite is the air-gapped pattern we can show. A new agency is a new authorization. I'll send an air-gapped test plan that includes the Gemini hallucination check Taylor asked for. If Distributed Cloud can host the model in that room, we point at it. If it can't, the plan says we stop and the client stays on our model. I will not write "Gemini everywhere" to make a partnership slide.
(00:06:48) Taylor Imaginary: Don't. I'll get in trouble for the slide I already want to make.
(00:06:52) Taylor Imaginary: Separately, yesterday Google Public Sector launched Gemini for government services, in preview, with launch partners. Sky, that's your August question. Want FDE4Real in as a partner?
(00:07:06) Sky Inventedson: Yes. As a deployment partner, not an integrator. Put it in the outline.
(00:07:11) Morgan Fakely: Taylor, say the commercial shape in one breath so I can hear it without the diagram.
(00:07:16) Taylor Imaginary: List FDE4Real in Gemini Enterprise. Co-sell into accounts where a field team is already in, or where we want one in. Gemini as a choice on their server. Our forward-deployed people and theirs can be in the same account. Referral rules written down so nobody trips. I owe you a draft of that outline by early November. Legal has to read it. They will be slow and they will be right about two things I haven't thought of.
(00:07:36) Damien Peters: Early November is a real date. I'll put "early November" in the note and not "soon."
(00:07:43) Sky Inventedson: I need the outline to say who staffs week one. If your specialist flies in for the kickoff and leaves, I'm not calling that co-sell. I'm calling that a cameo.
(00:07:56) Taylor Imaginary: Fair. The outline will name the cameo and the actual embed separately, so we can kill the cameo if it's embarrassing.
(00:08:06) Morgan Fakely: I read the pilot list. Northline, Harborlight, Red Kite, plus the rest of the book in the room. Sizes match what Damien previewed. GV could take up to 60 million of the round. I'm not offering that as a finished term. I'm telling you the number I can take to the partners without getting laughed at. The round you're describing is about 100. Sixty is a lead-sized bite. I know you're talking to other labs. I won't ask you to rank us on this call.
(00:08:44) Damien Peters: I appreciate the number being said out loud. We'd like one Google partner across the money and the channel. Two contracts is fine. Two strategies that fight each other is how this dies in a side letter.
(00:09:00) Morgan Fakely: Then we need to decide if the co-sell deal goes in the term sheet or beside it. I don't know yet. Taylor's outline has to exist before I can have the opinion. If I put a channel commitment in a term sheet before legal has seen it, the partner meeting will end early and not in a fun way.
(00:09:22) Damien Peters: So the order is, Taylor drafts, you read, then you tell us which envelope. Not the other way around. I can live with that if the Monday meeting isn't a surprise.
(00:09:34) Morgan Fakely: Monday is our partner meeting. Next Monday I'll take FDE4Real in. I will not promise you a term sheet on Tuesday. I will tell you what they flinched at.
(00:09:48) Sky Inventedson: What do you want from me before Monday, besides the test plan?
(00:09:54) Morgan Fakely: Deployment data for the top ten clients. Not a logo slide. Who's on site, how long, what's paid, what the survey did. If the top ten are all one sector, say so. I don't like discovering concentration in diligence.
(00:10:12) Sky Inventedson: You'll have it. A few of the top ten are logistics-adjacent to Northline and I won't hide the cluster. Health is Harborlight plus one smaller. Civic is Red Kite and it's not the revenue, it's the proof we can go dark.
(00:10:30) Damien Peters: And I'll send Morgan the cap table and the round's current terms. Current meaning what we've said to everyone, not a special Google price. If a term is still blank, the blank stays blank. Valuation is blank. I'm not filling it in because a meeting got friendly.
(00:10:52) Morgan Fakely: Blank is acceptable. Invented is not. Send it to me, not to the whole invite. Taylor doesn't need the cap table to draft a co-sell outline.
(00:11:04) Taylor Imaginary: I really don't. I get curious, and then I say a number in a meeting, and then Morgan looks at me like the calculator.
(00:11:14) Morgan Fakely: Correct.
(00:11:16) Damien Peters: Taylor, the banana-bread fixture. Did Sky run it?
(00:11:22) Sky Inventedson: We ran it yesterday. Our checker flagged the summary because the recording never mentioned flour. It did not flag it because it knows what a QBR is. That's the difference I care about. Genre shift is a smell. The test is still "is this in the audio."
(00:11:44) Taylor Imaginary: I'm unreasonably happy. Can I tell my CFO the sequel is "a different company's model noticed there was no flour"?
(00:11:54) Damien Peters: You can tell them a test fixture failed closed. No customer names, yours or ours. And it's our model, not Gemini. Don't let the sequel get better than the test.
(00:12:08) Taylor Imaginary: Spoil. Fine.
(00:12:12) Sky Inventedson: There's a hardware story Morgan asked for in the comments, the one about the prototype. I'll tell it once so it doesn't show up as a rumor. My dog, Kernel, ate prototype three. We logged it as a hardware failure, which was generous to the dog and accurate about the enclosure. Prototype four does not fit in a mouth. That's the pin you're buying, not the story. If this ends up in a partner memo, please use "enclosure," not "dog."
(00:12:48) Morgan Fakely: I'm using "dog." It's the only sentence I'll remember at 4 p.m.
(00:12:54) Damien Peters: The dog is not on the cap table.
(00:12:58) Sky Inventedson: The dog has equity in my patience. Separate topic. The next version you funded in your head, the factory. Damien mentioned it in September. It is not in market. The 35 million is the pin, the server, the deployments, the license. The factory is what the raise builds. If a partner asks "are the software factories live," the answer is no, there's a whiteboard in Denver I call the factory wall, and it has more questions than boxes.
(00:13:32) Taylor Imaginary: Good. I don't want to co-sell a whiteboard.
(00:13:36) Damien Peters: You'd be co-selling the thing that already has contracts. The whiteboard is why the round is this size and not a small extension. Does that land, or did I just reintroduce the pitch Sky told me not to do?
(00:13:52) Sky Inventedson: You did a small pitch. It was mostly true. I'll allow it.
(00:13:58) Morgan Fakely: Walk me through one top-ten account without naming a person. Northline. What do we get for the engagement.
(00:14:08) Sky Inventedson: Nine months, paid upfront. Team of forward-deployed engineers on their sites, pins on, server in their environment. Knowledge base of how freight exceptions actually get resolved, which was not the process on the poster. First use case shipped in week three, a reader that sits on top of that base. Satisfaction survey is theirs, the same one from the year before. The lift is in the pack. I'm not going to say 300 percent for Northline alone. The 300 is across the deployments that had a baseline. Northline is in that set. It is not the whole set.
(00:14:52) Morgan Fakely: Harborlight.
(00:14:54) Sky Inventedson: Six months. Child-safety review mattered and the papers are in the room. Filter list was theirs. Model calls stay inside their walls. They asked if a transcript could ever leave. It doesn't. Avery, on the other process, has talked to them. Damien told you that in September so it isn't a secret reference.
(00:15:18) Taylor Imaginary: Red Kite, short.
(00:15:21) Sky Inventedson: City. Air-gapped. Smaller dollars, longer argument with their security people, which is why it's useful to you. If we can't describe Red Kite, we can't describe your Distributed Cloud hope. The test plan will use that pattern, not a lab we control and then declare victory.
(00:15:44) Damien Peters: Open questions I want to leave with, so the note matches the call. One, does the co-sell sit inside the term sheet or beside it. Two, does Gemini on our server keep the near-zero rate. The test plan includes it, the answer is not in this meeting.
(00:16:04) Morgan Fakely: Add three, for me. Concentration in the top ten. Sky said they'll show it. If logistics is half the book, I need that before I say 60 in a room that writes things down.
(00:16:18) Sky Inventedson: You'll see the mix. I won't round it.
(00:16:22) Taylor Imaginary: And four, from me, softer. Who at your shop is allowed to tell a field team "yes, Gemini is fine here." If the answer is "Damien, on a Friday," I'll worry.
(00:16:36) Sky Inventedson: The answer is me, or a lead I name in the staffing plan. Damien can sell the choice. Damien cannot certify the room. He knows. We've had the fight.
(00:16:50) Damien Peters: We had the fight. Sky won. I certify nothing with a stamp on it.
(00:16:58) Morgan Fakely: Promises, so Damien's email doesn't invent any. Taylor, co-sell outline by early November. Me, partner meeting next Monday, and I'll report what they flinched at. I am not promising a term sheet.
(00:17:16) Damien Peters: Sky sends top-ten deployment data and the air-gapped test plan, with the Gemini check in it. I send Morgan the cap table and current terms, blanks left blank. I'll do it today. Subject line stays "as promised." If the cap table is in that email, Taylor, you'll get a separate note that just says the technical promises, so the cap table isn't in your thread.
(00:17:44) Taylor Imaginary: Thank you. I would have forwarded it. I'm self-aware about that and still not trustworthy.
(00:17:52) Sky Inventedson: I'll send the data tomorrow, not today. Today is a client review I already moved once. Tomorrow Denver morning. Taylor, I won't book you at 7.
(00:18:06) Taylor Imaginary: Denver morning is a gift. I'll read before I comment.
(00:18:12) Morgan Fakely: Damien, the other labs. I don't want terms. I want to know if a Monday flinch of "we might be slow" loses you. You said in September you want one partner per channel.
(00:18:26) Damien Peters: A slow Monday doesn't lose you. A silent month might. I'm not setting a fake deadline on this call. If another process puts a date on paper, I'll tell you the date exists without the terms. I'd rather you hear it from me than from a rumor with a drone in it.
(00:18:48) Taylor Imaginary: The drone founder. Don't.
(00:18:52) Damien Peters: I won't. Different meeting.
(00:18:56) Sky Inventedson: I have to go to that client review. Last thing. The pin in this call was on, because I wanted a clean transcript for our own knowledge base, on our server, not yours. If anyone said something they want out, say it before I stand up.
(00:19:16) Morgan Fakely: The dog stays in. The 60 stays in. Sundar's lines stay as small as they were.
(00:19:24) Taylor Imaginary: Banana bread stays. No customer name on my side either. There isn't one in this transcript, I checked while Sky was talking about flour.
(00:19:36) Damien Peters: Then we're good. Morgan, I'll send the cap table today. Sky, tomorrow. Taylor, early November on the outline, and you tell us when legal actually opens it.
(00:19:50) Morgan Fakely: I'll tell you after Monday, even if the answer is "they want another week." Thanks, both of you. Sky, the diagram was the first one this month I didn't have to translate.
(00:20:04) Sky Inventedson: Low bar. I'll take it. Bye.
(00:20:08) Taylor Imaginary: Bye.
(00:20:10) Damien Peters: Thanks, everyone.

(00:22:30) Morgan Fakely: Damien, you stayed again.
(00:22:34) Damien Peters: I did. It's becoming a bit. Two things I didn't want in the group. First, Sky uses they, and you did it right the whole time, thank you. Second, the 60. I'm not shopping that number to the other labs. If I say "up to 60" anywhere else, you can burn the term sheet we don't have yet.
(00:22:58) Morgan Fakely: I assumed. I'd rather hear you say it. The partner meeting will ask me if you're auctioning the lead. I'll say no, based on this.
(00:23:12) Damien Peters: Based on this, yes. I'll still tell you if a date shows up elsewhere. A date isn't a number.
(00:23:20) Morgan Fakely: A date I can use. A wink I can't. Go write the cap table email. And Damien, the duck. Was Due Diligence on this call?
(00:23:32) Damien Peters: He's on the shelf. He doesn't travel. Sky's dog has worse judgment and better name recognition. I'm a little worried Kernel is going to be the only fact that survives to your Monday.
(00:23:46) Morgan Fakely: Kernel and the flour. I'll try to add the filter. Goodbye.
(00:23:52) Damien Peters: Bye, Morgan.

(00:28:05) Sky Inventedson: You still recording?
(00:28:08) Damien Peters: The pin is. I thought you left for the client review.
(00:28:14) Sky Inventedson: I have six minutes. Don't put this in Morgan's email. The top ten, two of them are late on the satisfaction survey. The lift math doesn't include blanks. I don't want you to say "all ten came in" if I send a table with two holes.
(00:28:34) Damien Peters: I won't. Send the holes. Label them late, not zero.
(00:28:40) Sky Inventedson: And the factory wall. You described it fairly. There's one box I'm excited about and I'm not putting it in an investor transcript. Internal tooling for our own engineers, not a client product. If Taylor hears "factory" and thinks they can sell it this quarter, I'll be the cameo I complained about.
(00:29:04) Damien Peters: I'll keep the factory as "what the raise builds," not "what we co-sell." If I drift, correct me in the thread. You can be mean. Taylor likes you mean.
(00:29:16) Sky Inventedson: Taylor likes anyone who reads the pack. Low bar again. Okay. Client review. Pin can stay on until you close the laptop. Don't narrate your lunch.
(00:29:30) Damien Peters: No promises.

(00:36:12) Damien Peters: Note for the file, pin still on, Sky was right to warn me. Cap table goes to Morgan only, today. Top ten and the air-gapped plan from Sky tomorrow, holes labeled late. Taylor's outline, early November, legal in the path. Co-sell inside the term sheet or beside it, open. Gemini rate, open, test plan will include it. GV number I will not repeat elsewhere, up to 60 of a round around 100, not a term sheet. Sundar opened and left. No commitments from him, and I won't write any. Kernel ate prototype three. Do not lead with the dog. End note.
(00:37:02) [room tone. Recording ends 00:54:18 when the pin syncs and the laptop closes.]

## Talking points used (real, sourced)

- Google Public Sector launched Gemini for government services on 20 October 2026, in preview for US federal,
  state and local governments, with launch partners.
  https://www.googlecloudpresscorner.com/2026-10-20-Google-Public-Sector-Launches-Gemini-for-Government-Services
- Gemini Enterprise includes an agent finder where customers find and deploy thousands of agents reviewed for
  security and interoperability. Partners can sell their agents to Google Cloud customers.
  https://cloud.google.com/blog/products/ai-machine-learning/introducing-gemini-enterprise
- Google says its Google Distributed Cloud air-gapped product is authorized for US Government Secret and Top Secret
  missions, and Gemini is available on it.
  https://cloud.google.com/blog/products/ai-machine-learning/run-gemini-and-ai-on-prem-with-google-distributed-cloud
- In August 2025, GSA and Google announced Gemini for Government under OneGov, at $0.47 per agency through 2026.
  https://www.gsa.gov/about-us/newsroom/news-releases/gsa-google-announce-gemini-onegov-agreement-08212025
