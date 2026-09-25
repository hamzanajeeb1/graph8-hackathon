# graph8 Programmable Revenue Hackathon, Lahore

**Build the revenue machine that runs itself.**

Two days, one platform, every GTM capability you need already live behind an SDK and an API. Bring a laptop and a team. Leave with something that finds, reaches and closes customers on its own.

📅 **Saturday 26 and Sunday 27 September 2026, 12:00 PM to 8:00 PM PKT both days**
📍 **graph8 office at Kickstart, Lahore**
👥 **Teams of up to 3.** Solo builders welcome, we will help you find a team at kick-off.

---

## 🚀 About graph8

graph8 is a programmable revenue platform. Everything a B2B go-to-market team does, from finding a prospect to closing the deal, lives in one system and every piece of it is addressable by code and by AI agents.

**The platform, in one breath:**

- **CRM and data.** Contacts, companies, deals, lists, notes, tasks, custom objects and fields. Search across 700M+ contacts, enrich a person or company instantly, and watch intent signals, web visitors and hiring signals land on the record.
- **Outreach.** Multichannel sequences across email, SMS and LinkedIn, campaigns, newsletters, landing pages and forms, with deliverability, mailbox and domain management underneath.
- **Voice.** AI voice agents that answer, qualify, book and transfer. A power dialer with AI dispositions and coaching. Phone numbers, call recordings, transcripts and call results, all in the CRM.
- **Agents and workflows.** An agent runtime with skills, approvals and memory, a Work app where operator agents act on your behalf, a copilot, and a workflow engine that ties it together.
- **Meetings, marketplace and studio.** Scheduling and bookings, an SDR marketplace, and a studio for campaign content and knowledge.

**Two ways in:**

1. **`@graph8/sdk` on npm.** One `npm install`, typed clients for every module, plus a generated `g8.api` that covers every published operation. React bindings included.
2. **The Developer API.** The same 3,200+ operations under one contract, for any language: scoped API keys, webhooks with signed deliveries, and idempotent writes.

```typescript
import { g8 } from '@graph8/sdk';
g8.init({ apiKey: process.env.G8_API_KEY });

const leads = await g8.enrich.search([
  { field: 'seniority_level', operator: 'any_of', value: ['VP', 'Director'] },
  { field: 'company_industry', operator: 'contains', value: ['SaaS'] },
]);
const list = await g8.lists.create('Hackathon ICP', 'contacts');
await g8.lists.addContacts(list.id, leads.data.map((l) => l.id));
const [seq] = (await g8.sequences.list()).data;
await g8.sequences.add({ sequenceId: seq.id, listId: list.id });
```

Credentials, the demo workspace and the docs links will be handed out at kick-off.

---

## 🧠 What to build

Anything that makes revenue programmable. Pick a problem a sales or marketing team has on a Monday morning and build the thing that removes it. Some pointers to get you going:

- **Agents.** An SDR that works a list end to end. An operator that proposes actions and waits for a human yes. A voice agent that answers the phone, qualifies the caller and books the meeting.
- **Data.** Import a messy spreadsheet and land it as clean, enriched, deduplicated records. Rank accounts by intent, web visits and hiring signals. Turn a domain into a buying committee.
- **CRM.** Custom objects for a vertical. Deal health scores and next best action. A copilot that answers pipeline questions in plain language.
- **Pipelines.** Signal to list to sequence to task, with no human in the loop until a reply arrives. Lead routing with an audit trail. Workflows chained off graph8's webhooks.
- **Dialer.** Live coaching during the call. Dispositions and summaries written the moment it ends. A team leaderboard. Voicemail that gets callbacks.
- **Sequencer.** Sequences that branch on what the reply actually said. Deliverability checks before every send. Newsletter engagement turned into pipeline.
- **Voice.** Receptionists, reminders, callbacks, and twins that sound like your team.

That is a fraction of what is in the system. Meetings and bookings, forms and landing pages, mailboxes and domains, knowledge and studio content, the marketplace, tasks and notes, custom fields, webhooks and workflows are all in there too, and all reachable through the SDK. Explore it. The best builds usually come from a corner nobody pointed at.

---

## 🗓 Schedule (placeholder, times may shift)

### Saturday 26 September
- **12:00 PM** Doors open, setup, coffee
- **12:15 PM** Kick-off session and presentation: the platform, the SDK quick-start, the rules, and team formation
- **1:15 PM** Hacking begins
- **2:00 PM** Lunch
- **4:00 PM** Office hours: graph8 engineers on the floor for SDK and API questions
- **6:00 PM** Progress check, two minutes per team
- **7:30 PM** Wrap for the day, teams share blockers
- **8:00 PM** Close

### Sunday 27 September
- **12:00 PM** Doors open
- **12:15 PM** Stand-up, three items per team: shipped, next, blocked
- **12:30 PM** Hacking resumes
- **2:00 PM** Lunch
- **4:30 PM** Last office hours before freeze
- **5:30 PM** Code freeze and submissions
- **6:00 PM** Demos, five minutes per team, live and unrehearsed
- **7:15 PM** Judging and awards
- **8:00 PM** Close

---

## 🏆 Judging

Projects are scored on:

- **Technical execution.** Does it work, live, on the demo workspace?
- **Product thinking.** Is this something a sales or marketing team would actually use on Monday?
- **AI leverage and autonomy.** How much of the work happens without a human?
- **Revenue impact.** Does it find, reach or close customers better than what exists?
- **Use of the platform.** How much of graph8 did you put to work, and how well?
- **Demo quality.** Five minutes, no slides needed, show the thing.

**Prizes:** first, second and third place, plus special mentions for the best agent, the best voice build and the best data build. Details at kick-off.

---

## 🤝 Rules

- Teams of up to three. You can form a team at kick-off.
- Build on graph8: the SDK or the Developer API, in any language.
- Start fresh at kick-off. Existing libraries and boilerplate are fine, existing product code is not.
- Use the demo workspace and the credentials handed out at kick-off. Do not point a build at a live customer workspace.
- Demos must run live. A recording is a fallback, not a submission.
- Submit by code freeze on Sunday: a repo link, a one-paragraph description, and the name of the person demoing.

---

## 🎒 What to bring

- A laptop with Node 20+, or your language of choice for the API, and your editor.
- A GitHub account.
- Your own charger, headphones for the voice builds, and an appetite. Lunch is on us both days.

---

## 📬 Questions

Find Hamza or any graph8 engineer at the office, or drop a message in the hackathon channel. See you Saturday.
