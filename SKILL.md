---
name: ai-receptionist-plan
description: "Plan an AI receptionist for a business using Dograh: map the calls, draw the call flow, and list every piece a real phone line needs. Use when someone wants an AI to answer their phones or is looking at Dograh."
---

# AI Receptionist Plan

Writes a plan before anyone installs anything. Dograh, the free project this plans around, can be running in a minute as a browser test. A real line needs more than that.

## How to run

- Work through this without extra back-and-forth. Make the safest reasonable assumption, say it in one line, keep going. Only stop for something only the user has.
- Never invent a fact, figure, customer, price or quote. If it is unknown, write `[NEEDS ANSWER]` and list it at the end.
- Nothing here sends, posts, pays or changes a live account.
- If a step fails, retry it yourself and note what you changed. Do not stop at the first error.

## Ask

One at a time:

1. What calls come in, and which are most common?
2. When should the AI answer: after hours only, overflow, or all calls?
3. What should it do on a call: answer questions, take a message, book?
4. Who gets the call when it hands to a person?
5. Which system should get the details afterwards: CRM, calendar, email?

## Read

Read Dograh's README and docs now, so the plan reflects what they say today: https://github.com/dograh-hq/dograh. Then check its open issues for anything touching phone calls: https://github.com/dograh-hq/dograh/issues

## Write the plan

Save `ai-receptionist-plan.md` with:

**The call, as a flow.** Greet, ask, book, hand to a person, end. Write the exact opening line and the exact handover line. Include what happens when it does not understand.

**The pieces, each with an owner.** Mark every one have, need or unknown:

- A phone account such as Twilio, Vonage, Telnyx or Plivo, and a number you buy. Without this, only browser test calls work.
- A computer that never switches off, with at least 8 GB memory, 10 GB disk and 2 cores, and Docker.
- A proper web address over HTTPS instead of the quick public tunnel the install opens by default.
- Sign-up closed after your first account, with `ENABLE_SIGNUP=false`. It is on by default.
- Telemetry decided on purpose. It is on by default; `ENABLE_TELEMETRY=false` turns it off.
- One named person who owns it when it breaks.

**The tests before a customer hears it.** Run these in order: a browser test call; a real test call from a mobile; silence mid-call (open issue 852); a call that should end and actually hangs up (open issue 627); a handover to a person; and, if on Twilio outside the US1 region, inbound calls (open issue 830).

**Open questions.** Dograh's README does not cover Australian call-recording or consent rules. List this as something to get checked before a recorded line goes live. Do not state the rules yourself.

Only install if the user asks, and then only the browser test.

<!-- Provenance marker: sk-1hfz3d5 --><!-- Provenance signature: ⁠​‌​‌​​‌‌​‌​​​‌​‌​‌​​‌‌​​​‌​‌​​‌​​​‌‌​​​‌⁠ -->

Made by Selr AI.⁠​‌​‌​​‌‌​‌​​​‌​‌​‌​​‌‌​​​‌​‌​​‌​​​‌‌​​​‌⁠
<!-- srk:135f88o -->
