# graph8 Programmable Revenue Hackathon, Lahore

**Build the revenue machine that runs itself.**

Two days, one platform, every GTM capability you need already live behind an SDK, an API and an MCP server. Bring a laptop and a team. Leave with something that finds, reaches and closes customers on its own.

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

**Three ways in, pick whichever suits your build:**

1. **`@graph8/sdk` on npm.** One `npm install`, typed clients for every module, plus a generated `g8.api` that covers every published operation. React bindings included.
2. **The Developer API.** 3,200+ published operations under one contract, scoped API keys, webhooks with signed deliveries, and idempotent writes.
3. **The remote MCP server.** Paste `https://be.graph8.com/mcp/` into Claude Code, Cursor, Windsurf or ChatGPT, complete the browser sign-in, and your coding agent can drive graph8 directly through 370+ tools that it discovers at runtime.

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

Pick a theme, or combine two. Every idea below runs on surfaces that are live today. The surfaces named after each idea are where to start.

### 🤖 Agents
- **An SDR that works a list end to end.** Research each lead, write a first touch in the company's voice, enrol them in a sequence, and book the meeting when they reply. *Surfaces: enrich, sequences, inbox, meetings, agent runtime.*
- **An operator with approvals.** A Chief-of-Staff style agent that proposes actions in a channel, waits for a human yes, then executes. *Surfaces: Work app, agent runtime approvals, tasks.*
- **An inbound qualifier on the phone.** A voice agent that answers the company line, qualifies the caller, books time or transfers to the right person from the phone directory. *Surfaces: voice agents, phone directory, appointments.*

### 📊 Data
- **"Graphify it."** Drop a CSV or a spreadsheet, map the columns, enrich and dedupe every row, and land it as clean CRM records with an import run you can inspect. *Surfaces: enrich, contacts, companies, objects, lists.*
- **A signals dashboard.** Intent, web visitors and hiring signals for the accounts you care about, ranked into a daily call list. *Surfaces: signals, visitors, companies, lists.*
- **Enrichment as a product.** A tool that takes a domain and returns the buying committee, with confidence scores and sources. *Surfaces: enrich, companies, search.*

### 🗂 CRM
- **Custom objects for a vertical.** Model something graph8 does not have natively, such as partner deals, renewals or trial accounts, as custom objects with their own fields and views. *Surfaces: objects, fields, deals.*
- **Deal health and next best action.** Score every open deal from activity, replies and meetings, and tell the rep what to do next. *Surfaces: deals, notes, tasks, inbox, meetings.*
- **A revenue copilot for founders.** Ask questions about the pipeline in plain language and get answers with the records behind them. *Surfaces: copilot, deals, analytics.*

### 🔁 Pipelines
- **Signal to sequence in one flow.** A pipeline that turns a signal into a list, a list into a sequence enrolment, and a reply into a task, with no human in the loop until there is a reply. *Surfaces: signals, lists, sequences, webhooks, workflows.*
- **Lead routing.** Route new inbound leads by territory, size or intent to the right rep and the right sequence, with an audit trail. *Surfaces: forms, contacts, team, sequences, webhooks.*
- **Zapier, but yours.** A workflow builder that chains graph8 operations with other tools, using the webhook events graph8 already emits. *Surfaces: workflows, webhooks, integrations.*

### ☎️ Dialer
- **The coached dialer.** A power-dialer session where an AI listens, suggests the next question live, and writes the disposition and summary into the CRM the moment the call ends. *Surfaces: dialer sessions, dispositions, call artifacts, contacts.*
- **A team leaderboard.** Calls, connects, meetings booked, per rep and per day, with the recordings one click away. *Surfaces: dialer, voice call results, team.*
- **Voicemail that gets callbacks.** Personalised voicemail drops and a callback flow that reconnects the rep when the prospect rings back. *Surfaces: voice, phone numbers, inbound routing.*

### ✉️ Sequencer
- **Reply-aware sequences.** Branch a multichannel sequence on what the reply actually said, not just whether one arrived. *Surfaces: sequences, inbox, AI inbox tags.*
- **Deliverability guardrails.** A pre-send check on every step: domain health, warm-up state, spam words, send limits, with a clear go or no-go. *Surfaces: mailboxes, domains, deliverability, sequences.*
- **Newsletter to pipeline.** Turn newsletter engagement into scored leads and hand the hot ones to a sequence. *Surfaces: newsletter, contacts, lists, sequences.*

### 🧪 Weird stuff
- Build a whole product without leaving Cursor, using only the MCP server.
- A WhatsApp or Slack bot that runs a sales team's day.
- Anything that makes revenue programmable in a way we have not thought of.

---

## 🗓 Schedule (placeholder, times may shift)

### Saturday 26 September
- **12:00 PM** Doors open, setup, coffee
- **12:15 PM** Kick-off session and presentation: the platform, the SDK and MCP quick-start, the rules, and team formation
- **1:15 PM** Hacking begins
- **2:00 PM** Lunch
- **4:00 PM** Office hours: graph8 engineers on the floor for API, SDK and MCP questions
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

**Prizes:** first, second and third place, plus special mentions for the best use of MCP, the best voice build and the best data build. Details at kick-off.

---

## 🤝 Rules

- Teams of up to three. You can form a team at kick-off.
- Build on graph8: the SDK, the Developer API or the MCP server, in any combination, in any language.
- Start fresh at kick-off. Existing libraries and boilerplate are fine, existing product code is not.
- Use the demo workspace and the credentials handed out at kick-off. Do not point a build at a live customer workspace.
- Demos must run live. A recording is a fallback, not a submission.
- Submit by code freeze on Sunday: a repo link, a one-paragraph description, and the name of the person demoing.

---

## 🎒 What to bring

- A laptop with Node 20+ and your editor of choice. Cursor, Claude Code or Windsurf if you want to build through MCP.
- A GitHub account.
- Your own charger, headphones for the voice builds, and an appetite. Lunch is on us both days.

---

## 📬 Questions

Find Hamza or any graph8 engineer at the office, or drop a message in the hackathon channel. See you Saturday.
