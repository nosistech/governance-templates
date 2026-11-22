# AI Incident Response Playbook: Lumorra Data, Inc. (fictional example)

> **This is a fictional worked example.** Lumorra Data, Inc. does not exist. Any resemblance to a real company is a coincidence. It shows how a software company that builds AI into its product could adapt the [generic template](../generic/ai-incident-response-playbook.md). Ask your legal counsel to review your own process. This example is not legal advice.
>
> Open to use and adapt under the license.

| Document control | |
|---|---|
| Company | Lumorra Data, Inc.: a multi-tenant AI platform that lets mid-size companies search, summarize, and automate work on their own documents. About 45 staff, remote-first. |
| Playbook owner | Head of Security and Compliance |
| Approved by | Chief Executive Officer and Chief Technology Officer |
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

Lumorra has two kinds of AI incident. An incident can come from an AI tool that our staff use. It can also come from our product, and then it affects our customers. Product incidents also follow our customer contracts.

## 2. What counts as an AI incident

An **AI incident** is an event where an AI tool caused harm, or could have caused harm. The harm can be to people, to data, to money, to our work, or to trust in us.

An AI incident does not need an attacker. Many AI incidents come from a normal tool that gives a wrong answer, and a person who relies on it.

| Type | What it looks like | Example |
|---|---|---|
| Data exposure | The AI shows or sends data to the wrong people | Search shows one customer's document in another customer's workspace |
| Wrong output relied on | Someone acted on an AI answer that was false | A summary states a contract date that is not in the document |
| Unsafe or unfair output | The output can hurt someone, or treats a group unfairly | The help-center chatbot gives a rude or harmful answer to a customer's user |
| Agent action | An AI agent took an action that nobody intended | The workflow agent closes 300 tickets in a customer's help desk |
| Manipulation | Hidden instructions or planted false data change what the AI does | A shared document holds hidden instructions that tell the workflow agent to send files to an outside address |
| Vendor problem | The vendor has an outage, a breach, or changes its model without notice | A model provider retires a model version, and the answers change |
| Misuse | Someone uses AI against our rules, or to deceive | An engineer pastes customer content into a personal AI account |
| Stolen access or runaway cost | Someone uses our AI accounts or keys without permission | A model API key leaks in a public code repository, and the bill grows overnight |

**Prompt injection** is the technical name for "manipulation". The AI cannot always tell our instructions from text that it reads. A hidden line in a document can work like a forged note from the boss.

**Near misses** count too. A near miss is a problem that we caught before it harmed anyone. Record it in the log at severity 4. Near misses show where the next real incident will come from.

## 3. Roles

| Role | Who | Responsibilities |
|---|---|---|
| Incident lead | Head of Security and Compliance. Backup: Senior Site Reliability Engineer | Runs the response. Keeps the record. Decides the next step until the executive takes over. |
| Executive with switch-off authority | Chief Technology Officer. Backup: Chief Executive Officer | Confirms the severity. Approves a switch-off, the notices, and the public statements. |
| AI system owner | The product owner of the feature (AI-P01 to AI-P03), or the tool owner in the AI Tool Register | Knows how the tool works and who uses it. Helps to find the reach. |
| Technical responder | The on-call engineer (24/7 rotation) | Saves the evidence. Contains the tool. Checks the logs. |
| Privacy and legal contact | Head of Security and Compliance, with outside counsel | Decides with counsel which notices the law or a contract requires |
| Communications | Head of Customer Success (customers) and Chief Executive Officer (public) | Writes the messages to staff, customers, and the public |
| Vendor contact | The person who manages the vendor relationship | Calls the vendor. Asks for logs and answers. |

In a small company, one person can hold more than one role. Name a backup for the incident lead and for the executive. Incidents do not wait for holidays.

We write down the executive's switch-off authority in advance. In an incident, nobody should have to ask for permission to stop a tool that is causing harm.

## 4. Report a problem

Everyone at Lumorra reports AI problems. Report even if you are not sure that it is an incident. A false alarm costs a few minutes. A late report can cost much more.

If you see a problem with an AI tool:

1. Stop using the output. Do not send it, publish it, or act on it.
2. Do not delete anything. Keep the chat, the output, and the file.
3. Take a screenshot that shows the date and time.
4. Post it in the incident channel at once, or page the on-call engineer.
5. Write what you saw, which tool, when, and who else saw it.

Do not ask the AI tool to explain what went wrong. Its answer is a new guess, not a record of what happened.

Customers report through support. Support opens an incident at once for any report of another customer's data, an unexpected agent action, or a security concern.

We do not blame people for reports. We need to hear about mistakes early, including our own.

## 5. Severity

### 5.1 Rate each area

The incident lead rates the incident in 5 areas. Each area gets a level from 1 to 4. Level 1 is the most serious.

| Area | Level 1: Critical | Level 2: High | Level 3: Medium |
|---|---|---|---|
| People | Someone was harmed, or someone can be harmed now | A wrong or unfair output reached a person outside the company. No harm is confirmed yet. | A wrong output stayed inside the company |
| Data | Customer content reached another customer or anyone outside Lumorra | Customer content reached Lumorra staff without a support reason, or a vendor that should not have it | Internal data went to an unapproved AI tool |
| Money | Money moved without approval, or the loss is more than $50,000 | The loss is between $5,000 and $50,000 | The loss is less than $5,000 |
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
- for product incidents: the tenant IDs, the request IDs, and the search results behind each affected answer

Store the evidence in the incident folder on the security team's restricted drive. Only the incident lead and the people that the lead names can open it. Write each item and its location in the Timeline sheet.

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
| Turn off the feature flag for one customer, or for all customers | A product feature causes the problem |

**Switch-off criteria.** For each tool at the Deep tier, write down in advance when we switch it off. For example: "We turn off search if it shows one customer's document to another customer." The executive approves these criteria. When a criterion is met, the incident lead switches off the tool without a meeting. Record the criteria in the AI Tool Register.

A second criterion: "We turn off the workflow agent if it acts outside the connectors that a customer approved."

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

For a product incident, find every tenant and every request since the start date. Use the request logs, not only the customer reports.

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
| Did customer content or personal data reach the wrong people? | Our customers. They may then need to tell their own users. Counsel checks which laws apply. |
| Does a contract require notice? | Customers, under the incident clause in their contract and data processing agreement. Model providers, if their service is involved. |
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

Communications writes the messages. The executive approves every message that goes outside the company. For SEV1 and SEV2 product incidents, we also update the status page.

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
- **Product tests:** add the inputs that caused the incident to the tests that run before each release.
- **This playbook:** fix the steps that did not work.

Track each change in the incident log until its owner finishes it.

## 13. Practice

A playbook that nobody has practiced fails on the first real day. Practice once a year at least. Practice also after a big change, for example a new AI agent.

A practice session takes about 60 minutes. The incident lead describes a situation. The team talks through the steps in this playbook. Nobody touches a real system.

Example situations to start with:

- A customer reports that search shows a file from another company.
- The workflow agent reads a ticket with hidden instructions and tries to email files to an outside address.
- A model API key appears in a public code repository.

Record what was unclear, and update the playbook.

## 14. Keep the records

Keep the incident log, the timeline, the evidence, the notices, and the review for at least 6 years. Keep them longer if a law or a contract requires it. Limit access to the people who need it.

---

## Appendix A. Worked example: one customer sees another customer's document

This example follows the incidents in the Excel file. It is fictional.

**What happened (INC-01).** On Tuesday, October 20, a user at Customer A searched their workspace. One result showed the title and an excerpt of a document from Customer B.

| Time | Step | What Lumorra did |
|---|---|---|
| 14:05 | Report | Customer A sent a screenshot to support. |
| 14:12 | Report | Support opened an incident and paged the on-call engineer. |
| 14:18 | Rate | Data 1, trust and legal 1. Severity: SEV1. The CTO heard at once. |
| 14:24 | Evidence | The on-call engineer saved the request logs, the search settings, and the deploy history. |
| 14:31 | Contain | The switch-off criterion applied. The on-call engineer turned off search for all customers. The rest of the product kept working. |
| 16:40 | Reach | The team found the cause: Monday's release dropped the tenant ID from the search cache. |

**The reach.** The request logs since Monday's release showed 41 affected answers. Content from Customers B and D appeared in answers to Customers A and C.

**The notices.** Lumorra told all 4 customers within the time in their contracts, and told its insurer. The model provider was not involved, so no notice went to it. Counsel reviewed each decision.

**Fix and restart.** The team fixed the cache key and added a test that checks tenant separation in every release. Search came back for Lumorra's own workspace first, then for 5% of customers, then for everyone.

**A near miss (INC-02).** On November 12, the workflow agent read a shared document with hidden instructions. They told it to email the workspace files to an outside address. The approval step stopped the action, and the customer's admin reported it. Lumorra treated it as a security event too. The agent can now email only addresses that the customer approved.

**What changed after the reviews.**

- The AI Tool Register: AI-P01 and AI-P02 have new switch-off criteria and a higher risk.
- Product tests: a tenant separation test, and the hidden-instruction document, now run before each release.
- This playbook: support now pages the on-call engineer for any report of another customer's data.

## Appendix B. Security risks

The incident types in section 2 include risks from the [OWASP Top 10 for LLM Applications 2026](https://genai.owasp.org/resource/owasp-genai-llm-top-10-2026/).

The matching items are LLM01 Prompt Injection (manipulation), LLM02 Sensitive Information Disclosure (data exposure), and LLM03 Excessive Agency (agent action).

They also include LLM05 Data and Model Poisoning (planted false data), LLM06 Unbounded Consumption (runaway cost), and LLM07 Misinformation (wrong output relied on).

Laws and guidance change. This note is current as of November 2026.

---
*Fictional example by [NosisTech LLC](https://nosistech.com). Part of the [governance-templates](https://github.com/nosistech/governance-templates) collection. Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).*
