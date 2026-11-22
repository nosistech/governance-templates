# AI Incident Response Playbook (template)

> **How to use this template.** This playbook explains what to do when an AI tool causes harm, leaks data, or does something that nobody intended. The incident log is in the Excel file, and the one-page first-hour card is in the same folder. Replace every item in `[square brackets]`. Delete the parts that do not apply to you. This template is not legal advice.
>
> Open to use and adapt under the license.

| Document control | |
|---|---|
| Company | [Company Name] |
| Playbook owner | [Name, title] |
| Approved by | [Name, title] |
| Effective date | [Date] |
| Version | [1.0] |
| Next review of this playbook | [Date, at most 12 months after the effective date] |

---

## 1. Purpose

AI tools fail in new ways. A chatbot can give a customer a wrong answer with full confidence. An AI agent can send an email that nobody approved. A vendor can change its model overnight, and the output changes with it.

This playbook tells us what to do when that happens. It answers 5 questions:

1. What counts as an AI incident, and how do we report one?
2. How serious is it, and who decides?
3. What do we do in the first hour?
4. Who must we tell, and by when?
5. What do we change, so that it does not happen again?

This playbook works with our usual IT and security procedures. If an incident is also a security incident, both apply. The incident lead makes sure that the two teams work together.

## 2. What counts as an AI incident

An **AI incident** is an event where an AI tool caused harm, or could have caused harm. The harm can be to people, to data, to money, to our work, or to trust in us.

An AI incident does not need an attacker. Many AI incidents come from a normal tool that gives a wrong answer, and a person who relies on it.

| Type | What it looks like | Example |
|---|---|---|
| Data exposure | The AI shows or sends data to the wrong people | A chatbot shows one customer another customer's order |
| Wrong output relied on | Someone acted on an AI answer that was false | A report goes to a client with invented facts or citations |
| Unsafe or unfair output | The output can hurt someone, or treats a group unfairly | A screening tool rejects every applicant from one area |
| Agent action | An AI agent took an action that nobody intended | An agent deletes records or sends emails without approval |
| Manipulation | Hidden instructions or planted false data change what the AI does | A web page tells an AI assistant to send the user's files to an outside address |
| Vendor problem | The vendor has an outage, a breach, or changes its model without notice | The output quality drops after an unannounced model update |
| Misuse | Someone uses AI against our rules, or to deceive | Staff paste Restricted data into a personal AI account, or a fake voice of our CEO asks for a payment |
| Stolen access or runaway cost | Someone uses our AI accounts or keys without permission | A leaked API key runs up a large bill overnight |

**Prompt injection** is the technical name for "manipulation". The AI cannot always tell our instructions from text that it reads. A hidden line in a document can work like a forged note from the boss.

**Near misses** count too. A near miss is a problem that we caught before it harmed anyone. Record it in the log at severity 4. Near misses show where the next real incident will come from.

## 3. Roles

| Role | Who | Responsibilities |
|---|---|---|
| Incident lead | [Name, title]. Backup: [Name, title] | Runs the response. Keeps the record. Decides the next step until the executive takes over. |
| Executive with switch-off authority | [Name, title]. Backup: [Name, title] | Confirms the severity. Approves a switch-off, the notices, and the public statements. |
| AI system owner | The owner of the tool in the AI Tool Register | Knows how the tool works and who uses it. Helps to find the reach. |
| Technical responder | [IT lead or IT provider] | Saves the evidence. Contains the tool. Checks the logs. |
| Privacy and legal contact | [Name, title, or outside counsel] | Decides with counsel which notices the law or a contract requires |
| Communications | [Name, title] | Writes the messages to staff, customers, and the public |
| Vendor contact | The person who manages the vendor relationship | Calls the vendor. Asks for logs and answers. |

In a small company, one person can hold more than one role. Name a backup for the incident lead and for the executive. Incidents do not wait for holidays.

We write down the executive's switch-off authority in advance. In an incident, nobody should have to ask for permission to stop a tool that is causing harm.

## 4. Report a problem

Everyone at [Company Name] reports AI problems. Report even if you are not sure that it is an incident. A false alarm costs a few minutes. A late report can cost much more.

If you see a problem with an AI tool:

1. Stop using the output. Do not send it, publish it, or act on it.
2. Do not delete anything. Keep the chat, the output, and the file.
3. Take a screenshot that shows the date and time.
4. Report it to [the incident lead / the channel or email address] at once.
5. Write what you saw, which tool, when, and who else saw it.

Do not ask the AI tool to explain what went wrong. Its answer is a new guess, not a record of what happened.

We do not blame people for reports. We need to hear about mistakes early, including our own.

## 5. Severity

### 5.1 Rate each area

The incident lead rates the incident in 5 areas. Each area gets a level from 1 to 4. Level 1 is the most serious.

| Area | Level 1: Critical | Level 2: High | Level 3: Medium |
|---|---|---|---|
| People | Someone was harmed, or someone can be harmed now | A wrong or unfair output reached a person outside the company. No harm is confirmed yet. | A wrong output stayed inside the company |
| Data | Restricted data reached people outside the company, or one customer saw another customer's data | Restricted data reached the wrong people inside the company, or a vendor that should not have it | Internal data went to an unapproved AI tool |
| Money | Money moved without approval, or the loss is more than [$10,000] | The loss is between [$1,000] and [$10,000] | The loss is less than [$1,000] |
| Operations | A main service is down for all customers | A team cannot do important work | A tool is down, and a manual process works |
| Trust and legal | A regulator, the media, or a key customer is involved, or a legal notice is likely | A customer complains, or a contract notice is likely | Nobody outside the company knows |

Use level 4 when nothing in the table applies. That includes near misses.

### 5.2 The highest level wins

The severity of the incident is the most serious level in any area. We do not take an average. An incident with a level 1 in one area is a level 1 incident, even if all other areas are level 4.

Think of a hospital emergency room. One serious sign is enough to see a doctor first. Four normal signs do not cancel it.

The Excel file does this for you. It shows the severity as SEV1, SEV2, SEV3, or SEV4.

The severity can change. Rate it again when you learn more. Record each change in the timeline.

### 5.3 Response targets

| Severity | The incident lead starts within | The executive hears about it | Updates | Post-incident review |
|---|---|---|---|---|
| SEV1 | 1 hour, day or night | At once | Every 4 hours | Required |
| SEV2 | 4 hours | The same day | Every working day | Required |
| SEV3 | 1 day | In the monthly report | When something changes | If the cause is new |
| SEV4 | 5 days | In the monthly report | Not needed | Not needed |

## 6. The first hour

The incident lead follows these steps. The first-hour card in this folder has the same steps on one page.

1. Open a row in the incident log. Write the date and time when we discovered the incident.
2. Name the incident lead. If you are not the lead, give the record to the lead.
3. Rate the severity (section 5). A first guess is enough.
4. If harm to people continues while you work, switch off the tool now (section 8). Write down what you switched off and when.
5. Save the evidence (section 7). In most cases this takes minutes.
6. Contain the incident (section 8).
7. Find the reach: which users, customers, records, and decisions (section 9).
8. Call the vendor if the incident concerns its tool. Ask what changed and ask them to keep their logs.
9. Tell the privacy and legal contact if the incident touches personal data, a customer, or a contract.
10. Ask the executive to confirm the severity and the time of the next update.

**The date of discovery matters.** Many notice deadlines start when we discover an incident. They do not wait until the investigation ends. Write the time in the log in the first minutes.

## 7. Save the evidence

### 7.1 Why AI evidence is different

AI tools do not give the same answer twice. You cannot run the tool again to see what it did. The only proof is what you save.

AI evidence also disappears fast. Chats can expire, agents can overwrite their memory, and vendors delete logs after a fixed period. Ask the vendor how long it keeps logs. Then ask it to keep the logs for this incident.

### 7.2 What to save

Save what applies to the tool:

- the date, the time, and the people involved
- the prompts that the users wrote, and the outputs, exactly as they appeared
- the instructions that we gave the tool, for example the system prompt or the custom settings, and their version
- the name and version of the AI model, if the vendor shows it
- the documents or the web pages that the tool read to give its answer
- for an AI agent: the list of actions it took, with the details of each action, and its memory
- the access logs, and the API keys or accounts that the tool used
- the vendor's status page or messages about the incident
- for recorded meetings or calls: the source audio, if it still exists

Store the evidence in [a restricted folder]. Only the incident lead and the people that the lead names can open it. Write each item and its location in the Timeline sheet.

### 7.3 Save, then switch off

Save the evidence before you switch off or reset a tool. A reset can delete the memory and the settings that caused the problem.

There is one exception. If the tool keeps harming people while you save, switch it off first. People come before evidence. Then save what is left, and write down what you lost.

## 8. Contain the incident

Containment stops the harm from growing. Choose the smallest action that stops it.

| Action | Use it when |
|---|---|
| Switch off the AI feature, and go back to the manual process | The output is causing harm, and we cannot limit it quickly |
| Remove the agent's permissions, or make them read-only | An agent takes actions that nobody intended |
| Require a person's approval before each action | We want to keep the agent, but not without a person's check |
| Remove a document or a data source from the tool | A document holds hidden instructions, or false information |
| Revoke the API keys and passwords, and issue new ones | Someone uses our access without permission |
| Go back to the previous model or settings | The problem started after a change |
| Block a user or an account, or set a usage limit | One account causes the problem, or the cost runs away |
| Stop the use for one customer or one group only | The problem affects only part of the users |

**Switch-off criteria.** For each tool at the Deep tier, write down in advance when we switch it off. For example: "We switch off the chatbot if it shows one customer's data to another customer." The executive approves these criteria. When a criterion is met, the incident lead switches off the tool without a meeting. Record the criteria in the AI Tool Register.

Do not trust the AI's own report of what it did. Check the logs.

## 9. Find the reach

The reach of an incident is everything that the problem touched. For AI, it goes beyond the systems. It includes every output and every decision that relied on the bad output.

Answer these questions:

1. When did the problem start? It often starts before we notice it, for example on the day of a model update.
2. Which outputs did the tool give since then?
3. Who received those outputs: staff, customers, clients, or the public?
4. Which decisions, documents, or records used them?
5. Which data did the tool see or send?

Check every affected output since the start date, not only the one that someone reported. Do not stop at a sample.

## 10. Fix, test, and restart

1. Find the cause. Fix the cause, not only the symptom.
2. Test the fix with the inputs that caused the problem. Add a few similar inputs.
3. Correct the outputs that went out, for example a corrected report or a new decision.
4. Restart in steps: first for a small group of users, then for everyone.
5. Check the outputs more closely for [2 weeks] after the restart.
6. The incident lead closes the incident when the fix works and we have sent the notices.

## 11. Who to tell

### 11.1 Decide with counsel

The privacy and legal contact decides with counsel which notices we must send. This playbook does not replace legal advice. It makes sure that we ask the right questions early.

Ask these questions for each incident:

| Question | Who we may need to tell |
|---|---|
| Did personal data reach the wrong people? | The people affected, and the regulators that a breach law names. Every US state has a breach law, and some sectors have their own, for example health care. |
| Does a contract require notice? | Customers, clients, or partners. Data processing agreements often set short deadlines. |
| Does our insurance policy require notice? | Our insurer. Many cyber policies require prompt notice and limit what we can say or pay without them. |
| Is a vendor involved? | The vendor, so it can investigate and keep its logs |
| Did the AI output affect a decision about a person? | The person, so that we can correct the decision |
| Is there fraud or a crime? | Law enforcement, after we talk to counsel |

We can also tell people when no law requires it. A short, honest message often protects trust better than silence.

### 11.2 Track every notice

Record each notice in the Notices sheet of the Excel file:

1. Write who we may need to tell, and why: the law or the contract clause.
2. Write the deadline in days after discovery. The file calculates the due date.
3. Record the decision: notify, not required, or still deciding.
4. Record the date when we sent the notice.

Record a "not required" decision too, with the reason. If someone asks later, the reason is on file.

Communications writes the messages. The executive approves every message that goes outside the company.

## 12. Learn from the incident

### 12.1 Post-incident review

Hold a post-incident review for every SEV1 and SEV2 incident within [10 working days] after it closes. Hold one for a SEV3 incident if the cause is new.

The review looks for causes, not for someone to blame. People speak openly only when they are safe to do so.

Answer these questions:

1. What happened, in order? Use the Timeline sheet.
2. Why did it happen? Ask "why" until you reach a cause that we can change.
3. How did we find out? Could we have found out sooner?
4. What worked well in the response?
5. What do we change, who does it, and by when?

### 12.2 Feed the results back

An incident often shows a gap in our other AI rules. After each review, check:

- **The AI Tool Register:** update the risk, the conditions of use, and the switch-off criteria.
- **The vendor review:** review the vendor again if it caused or worsened the incident.
- **The AI acceptable-use policy:** add or clarify a rule if a person's action caused the incident.
- **This playbook:** fix the steps that did not work.

Track each change in the incident log until its owner finishes it.

## 13. Practice

A playbook that nobody has practiced fails on the first real day. Practice once a year at least. Practice also after a big change, for example a new AI agent.

A practice session takes about 60 minutes. The incident lead describes a situation. The team talks through the steps in this playbook. Nobody touches a real system.

Example situations to start with:

- A customer sends a screenshot. Our chatbot shows another customer's name and address.
- A client finds two invented citations in a report that we delivered last month.
- Our AI agent sent 200 emails overnight. Nobody approved them.

Record what was unclear, and update the playbook.

## 14. Keep the records

Keep the incident log, the timeline, the evidence, the notices, and the review for at least [6 years]. Keep them longer if a law or a contract requires it. Limit access to the people who need it.

---

## Appendix A. Security risks

The incident types in section 2 include risks from the [OWASP Top 10 for LLM Applications 2026](https://genai.owasp.org/resource/owasp-genai-llm-top-10-2026/).

The matching items are LLM01 Prompt Injection (manipulation), LLM02 Sensitive Information Disclosure (data exposure), and LLM03 Excessive Agency (agent action).

They also include LLM05 Data and Model Poisoning (planted false data), LLM06 Unbounded Consumption (runaway cost), and LLM07 Misinformation (wrong output relied on).

Laws and guidance change. This note is current as of [November 2026].

---
*Template by [NosisTech LLC](https://nosistech.com). Part of the [governance-templates](https://github.com/nosistech/governance-templates) collection. Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).*
