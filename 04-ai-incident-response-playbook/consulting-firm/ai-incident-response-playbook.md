# AI Incident Response Playbook: Keystone Advisory (fictional example)

> **This is a fictional worked example.** Keystone Advisory does not exist. Any resemblance to a real company is a coincidence. It shows how a small consulting firm could adapt the [generic template](../generic/ai-incident-response-playbook.md). Ask your legal counsel to review your own process. This example is not legal advice.
>
> Open to use and adapt under the license.

| Document control | |
|---|---|
| Company | Keystone Advisory: a remote consulting firm with 12 consultants. It advises mid-size companies on operations, finance, and technology. |
| Playbook owner | Operations Manager |
| Approved by | Managing Partner |
| Effective date | October 1, 2026 |
| Version | 1.0 |
| Next review of this playbook | September 30, 2027 |

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

Our name is on every page that we deliver. A wrong fact in a client report is an incident, even when no data leaves the firm.

## 2. What counts as an AI incident

An **AI incident** is an event where an AI tool caused harm, or could have caused harm. The harm can be to people, to data, to money, to our work, or to trust in us.

An AI incident does not need an attacker. Many AI incidents come from a normal tool that gives a wrong answer, and a person who relies on it.

| Type | What it looks like | Example |
|---|---|---|
| Data exposure | The AI shows or sends data to the wrong people | The notetaker emails a meeting summary to a person at another client |
| Wrong output relied on | Someone acted on an AI answer that was false | A client report cites three sources that do not exist |
| Unsafe or unfair output | The output can hurt someone, or treats a group unfairly | An AI summary of staff interviews describes one group of employees unfairly |
| Agent action | An AI agent took an action that nobody intended | The email assistant sends a reply to a client before the consultant reviews it |
| Manipulation | Hidden instructions or planted false data change what the AI does | A web page plants false figures that the research tool repeats as facts |
| Vendor problem | The vendor has an outage, a breach, or changes its model without notice | The research tool's answers get worse after an unannounced model update |
| Misuse | Someone uses AI against our rules, or to deceive | A consultant uses a personal AI account with a client's financial data |
| Stolen access or runaway cost | Someone uses our AI accounts or keys without permission | Someone uses a former consultant's AI account after they left |

**Prompt injection** is the technical name for "manipulation". The AI cannot always tell our instructions from text that it reads. A hidden line in a document can work like a forged note from the boss.

**Near misses** count too. A near miss is a problem that we caught before it harmed anyone. Record it in the log at severity 4. Near misses show where the next real incident will come from.

## 3. Roles

| Role | Who | Responsibilities |
|---|---|---|
| Incident lead | Operations Manager. Backup: a senior consultant named each year | Runs the response. Keeps the record. Decides the next step until the executive takes over. |
| Executive with switch-off authority | Managing Partner. Backup: the Operations Manager | Confirms the severity. Approves a switch-off, the notices, and the public statements. |
| AI system owner | The owner of the tool in the AI Tool Register | Knows how the tool works and who uses it. Helps to find the reach. |
| Technical responder | Our managed IT provider | Saves the evidence. Contains the tool. Checks the logs. |
| Privacy and legal contact | Managing Partner, with outside counsel | Decides with counsel which notices the law or a contract requires |
| Communications | The engagement lead for the client, with the Managing Partner | Writes the messages to staff, customers, and the public |
| Vendor contact | Operations Manager | Calls the vendor. Asks for logs and answers. |

In a small company, one person can hold more than one role. Name a backup for the incident lead and for the executive. Incidents do not wait for holidays.

We write down the executive's switch-off authority in advance. In an incident, nobody should have to ask for permission to stop a tool that is causing harm.

## 4. Report a problem

Everyone at Keystone reports AI problems. Report even if you are not sure that it is an incident. A false alarm costs a few minutes. A late report can cost much more.

If you see a problem with an AI tool:

1. Stop using the output. Do not send it, publish it, or act on it.
2. Do not delete anything. Keep the chat, the output, and the file.
3. Take a screenshot that shows the date and time.
4. Report it to the Operations Manager at once, by phone or in the operations channel.
5. Write what you saw, which tool, when, and who else saw it.

Do not ask the AI tool to explain what went wrong. Its answer is a new guess, not a record of what happened.

We do not blame people for reports. We need to hear about mistakes early, including our own.

## 5. Severity

### 5.1 Rate each area

The incident lead rates the incident in 5 areas. Each area gets a level from 1 to 4. Level 1 is the most serious.

| Area | Level 1: Critical | Level 2: High | Level 3: Medium |
|---|---|---|---|
| People | Someone was harmed, or someone can be harmed now | A wrong or unfair output reached a person outside the company. No harm is confirmed yet. | A wrong output stayed inside the company |
| Data | Client data reached another client or anyone outside Keystone | Client data reached a consultant outside the engagement, or a vendor that should not have it | Internal data went to an unapproved AI tool |
| Money | Money moved without approval, or the loss is more than $10,000 | The loss is between $1,000 and $10,000 | The loss is less than $1,000 |
| Operations | We cannot deliver to a client on time | A team cannot do important work | A tool is down, and a manual process works |
| Trust and legal | A regulator, the media, or a key client is involved, or a legal notice is likely | A client complains, or a contract notice is likely | Nobody outside the company knows |

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
- for client deliverables: every version of the document, and the AI chats that helped to draft it

Store the evidence in the restricted Incidents folder in our document system. Only the incident lead and the people that the lead names can open it. Write each item and its location in the Timeline sheet.

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

**Switch-off criteria.** For each tool at the Deep tier, write down in advance when we switch it off. For example: "We disconnect the email assistant if it sends a client message without a consultant's approval." The executive approves these criteria. When a criterion is met, the incident lead switches off the tool without a meeting. Record the criteria in the AI Tool Register.

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

For a client deliverable, check every deliverable since the start date that used the same tool or the same AI-drafted material.

## 10. Fix, test, and restart

1. Find the cause. Fix the cause, not only the symptom.
2. Test the fix with the inputs that caused the problem. Add a few similar inputs.
3. Correct the outputs that went out, for example a corrected report or a new decision.
4. Restart in steps: first for a small group of users, then for everyone.
5. Check the outputs more closely for 2 weeks after the restart.
6. The incident lead closes the incident when the fix works and we have sent the notices.

## 11. Who to tell

### 11.1 Decide with counsel

The privacy and legal contact decides with counsel which notices we must send. This playbook does not replace legal advice. It makes sure that we ask the right questions early.

Ask these questions for each incident:

| Question | Who we may need to tell |
|---|---|
| Did client data or personal data reach the wrong people? | The client, and the people affected. Breach laws can apply. Counsel decides. |
| Does a contract require notice? | The client, under the engagement letter or the client's data agreement. |
| Does our insurance policy require notice? | Our professional liability insurer and our cyber insurer. Many policies require prompt notice and limit what we can say or pay without them. |
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

Hold a post-incident review for every SEV1 and SEV2 incident within 10 working days after it closes. Hold one for a SEV3 incident if the cause is new.

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
- **Quality review:** add the check that failed to the review steps for AI-assisted work.
- **This playbook:** fix the steps that did not work.

Track each change in the incident log until its owner finishes it.

## 13. Practice

A playbook that nobody has practiced fails on the first real day. Practice once a year at least. Practice also after a big change, for example a new AI agent.

A practice session takes about 60 minutes. The incident lead describes a situation. The team talks through the steps in this playbook. Nobody touches a real system.

Example situations to start with:

- A client finds two sources in our report that do not exist.
- The notetaker sends a meeting summary to a person at another client.
- A consultant finds client data in a personal AI account.

Record what was unclear, and update the playbook.

## 14. Keep the records

Keep the incident log, the timeline, the evidence, the notices, and the review for at least 6 years. Keep them longer if a law or a contract requires it. Limit access to the people who need it.

---

## Appendix A. Worked example: invented citations in a client report

This example follows the incident in the Excel file (INC-01). It is fictional.

**What happened.** On Monday, November 9, a client's finance director emailed the engagement lead. Three sources in our October report did not exist.

| Time | Step | What Keystone did |
|---|---|---|
| 10:05 | Report | The engagement lead read the email and kept it. |
| 10:20 | Report | The engagement lead called the Operations Manager. |
| 10:35 | Rate | People 2, money 3, trust and legal 2. Severity: SEV2. The Managing Partner heard the same day. |
| 10:50 | Evidence | The Operations Manager saved every version of the report and the consultant's chats in the business AI account. |
| 12:00 | Contain | We held every deliverable with AI-drafted material until someone checked its sources. We did not switch off the chat assistant. |

**The reach.** Since September 1, 9 deliverables used AI-drafted material. Two consultants checked every source in all 9. They found one more invented source, in a report for another client.

**The notices.** The engagement leads sent both clients a corrected report with a short, honest note. The Managing Partner told the professional liability insurer. Counsel reviewed the messages first.

**Fix and restart.** Every AI-assisted deliverable now gets a source check before it goes out. Someone other than the author does the check. All consultants did a 30-minute training on the new step.

**What changed after the review.**

- The quality review: it checked the conclusions, but nobody owned the sources. Now the source check is a named step.
- The AI acceptable-use policy: it now says that a person checks every source that an AI tool suggests.
- The AI Tool Register: the chat assistant keeps its approval, with the source check as a condition of use.

## Appendix B. Security risks

The incident types in section 2 include risks from the [OWASP Top 10 for LLM Applications 2026](https://genai.owasp.org/resource/owasp-genai-llm-top-10-2026/).

The matching items are LLM01 Prompt Injection (manipulation), LLM02 Sensitive Information Disclosure (data exposure), and LLM03 Excessive Agency (agent action).

They also include LLM05 Data and Model Poisoning (planted false data), LLM06 Unbounded Consumption (runaway cost), and LLM07 Misinformation (wrong output relied on).

Laws and guidance change. This note is current as of November 2026.

---
*Fictional example by [NosisTech LLC](https://nosistech.com). Part of the [governance-templates](https://github.com/nosistech/governance-templates) collection. Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).*
