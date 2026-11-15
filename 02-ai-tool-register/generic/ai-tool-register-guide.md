# AI Tool Register: Guide (template)

> **How to use this template.** This guide explains how to keep your AI Tool Register. The register itself is the Excel file in the same folder. Replace every item in `[square brackets]`. Delete the parts that do not apply to you. This template is not legal advice.
>
> Free to use and adapt.

| Document control | |
|---|---|
| Company | [Company Name] |
| Register owner | [Name, title] |
| Approved by | [Name, title] |
| Effective date | [Date] |
| Version | [1.0] |
| Next review of this guide | [Date, at most 12 months after the effective date] |

---

## 1. Purpose

The AI Tool Register is the list of every AI tool that [Company Name] uses, with a risk score for each use. It answers 4 questions:

1. Which AI tools do we use, and for what?
2. Who is responsible for each one?
3. How risky is each use?
4. Is each use approved, approved with conditions, or not allowed?

Our AI Acceptable-Use Policy tells staff to use only approved tools. This register is where we write down "approved". When a customer, an auditor, or an insurer asks "which AI do you use?", this register is the answer.

## 2. What goes in the register

### 2.1 One row for each use, not for each vendor
The same tool can be safe for one task and risky for another. A chat assistant that drafts internal emails is low risk. The same chat assistant that drafts answers to customers about their accounts is higher risk. Give each use its own row.

### 2.2 Include all of these
- AI tools that the company pays for, for example chat assistants and code assistants
- AI features inside software that we already use, for example email, documents, CRM, phone systems, and design tools
- meeting recorders and AI notetakers
- browser extensions and AI browsers
- AI agents that can take actions, and AI tools connected to our systems
- AI inside products or services that we sell to customers
- free or personal AI accounts that staff use for work, with the status "Prohibited", so that the decision is on record

### 2.3 What you do not need to register
[List the AI features that you exempt, for example spell check and grammar suggestions that do not send data outside the software. Keep this list short. If you are not sure, register the feature.]

## 3. Roles

| Role | Who | Responsibilities |
|---|---|---|
| Register owner | [Name, title] | Keeps the register complete and current. Runs the reviews. Reports to leadership. |
| Tool owner | One named person for each row | Knows how the tool is used. Keeps the row correct. Can switch the tool off. |
| Approver | Depends on the risk level (see section 7) | Decides on each use |
| All staff | Everyone | Ask before you use a new tool or a new use. Report AI tools that are not in the register. |

## 4. How a new use gets into the register

1. A person fills in the AI Tool Request Form and sends it to [the register owner / channel].
2. The register owner adds a row with the status "Under review".
3. The register owner and the tool owner score the risk (section 6).
4. The approver for that risk level decides (section 7).
5. The register owner records the decision, the conditions, the approver, and the date.
6. The register owner tells the person who asked. We decide within [5] business days.

## 5. The columns

| Column | What to write | Example |
|---|---|---|
| ID | A unique number | AI-007 |
| Tool and plan | The product name and the plan. The plan matters: free and business plans often have different data terms. | [Chat assistant], business plan |
| Vendor | The company that provides the tool | [Vendor name] |
| What we use it for | The task, in one sentence | Draft replies to customer support emails |
| Type of AI | Choose from the list | AI feature in existing software |
| Tool owner | One named person | [Name, title] |
| Who uses it | Teams and approximate number of people | Support team, 8 people |
| Highest data tier | The most sensitive data that the tool sees: Public, Internal, or Restricted. Our AI Acceptable-Use Policy, section 5, defines the tiers. | Restricted |
| Affects decisions about people? | Yes, if the output helps to decide about hiring, pay, credit, health care, housing, insurance, or education | No |
| Human check | How a person checks the output | Person reviews before use |
| Vendor terms: no training on our data? | Yes, No, or Unknown. Check the contract, not the marketing page. | Yes |
| Likelihood | 1 to 5 (section 6) | 3 |
| Impact | 1 to 5 (section 6) | 4 |
| Risk score | Calculated: likelihood × impact | 12 |
| Risk level | Calculated: Low, Medium, High, or Critical | High |
| Controls in place | What we do today to lower the risk | Business plan; agent sees only its own queue; a person approves each reply |
| Status | Approved, Approved with conditions, Under review, Prohibited, or Retired | Approved with conditions |
| Conditions of use | The rules that apply to this use | Restricted data only from the support system. No refunds or account changes. |
| Approved by | Name and title | [Name, title] |
| Decision date | The date of the decision | [Date] |
| Next review | Calculated from the decision date and the risk level | [Date] |

## 6. How to score the risk

### 6.1 Ask "what could go wrong?"
For each use, write down the worst thing that could credibly happen. Use these common AI risks as a checklist:

- **Data leaks:** the tool exposes our data or our customers' data.
- **Wrong output:** the tool invents facts, sources, or numbers, and someone relies on them.
- **Unfair results:** the output treats a group of people unfairly.
- **Hidden instructions:** a website, an email, or a document tells the AI tool to do something harmful. Experts call this "prompt injection".
- **Too much power:** an agent sends, deletes, buys, or changes something that nobody approved.
- **Vendor problems:** the vendor changes its terms, its model, or its prices, or it has a breach.

### 6.2 Likelihood: how probable is the harm in the next 12 months?

| Score | Name | Meaning |
|---|---|---|
| 1 | Rare | We do not expect it in the next 12 months. |
| 2 | Unlikely | It could happen once in several years. |
| 3 | Possible | It could happen about once a year. |
| 4 | Likely | It could happen several times a year. |
| 5 | Almost certain | It happens every month, or it already happened here. |

Score the chance that the harm reaches someone, not the chance of a small error. AI tools make small errors every day. A person who checks the output stops most of them.

### 6.3 Impact: how bad is the worst credible case?

| Score | Name | Meaning |
|---|---|---|
| 1 | Negligible | A small fix that nobody outside the team notices |
| 2 | Minor | Internal rework. No personal data and no customer sees it. |
| 3 | Moderate | An error reaches a customer and we correct it, or a small amount of personal data is exposed |
| 4 | Major | Harm to a person, a breach that we must report, questions from a regulator, or the loss of an important customer |
| 5 | Severe | Serious harm to a person, a large data breach, or a fine or loss that threatens the business |

### 6.4 Calculate the score and the level

**Risk score = likelihood × impact.** The result is a number from 1 to 25. The Excel file calculates it for you.

| Score | Risk level |
|---|---|
| 1–4 | Low |
| 5–9 | Medium |
| 10–15 | High |
| 16–25 | Critical |

### 6.5 Scoring rules
1. Score the use as it runs today, with the controls that are really in place. A control that is only planned does not count yet.
2. If you are not sure between two numbers, choose the higher one.
3. If the use affects decisions about people, the impact is at least 4.
4. If the tool sees Restricted data and the vendor terms are "Unknown", the impact is at least 4.
5. Two people score each High or Critical use: the tool owner and the register owner.

## 7. Decisions

### 7.1 Who decides

| Risk level | Who approves | What the approver does |
|---|---|---|
| Low | [Tool owner or manager] | Approves with the standard rules in our AI Acceptable-Use Policy |
| Medium | [Policy owner / IT lead] | Approves with written conditions of use |
| High | [AI review group] | Approves only with conditions and a written plan to lower the score |
| Critical | Nobody, until the score goes down | Change the use or add controls until the score is 15 or lower. Only [the CEO] can accept a Critical risk, in writing, for a limited time. |

### 7.2 Status

| Status | Meaning |
|---|---|
| Approved | Staff can use the tool for this use, under our AI Acceptable-Use Policy. |
| Approved with conditions | Staff can use it, but only under the conditions in the row. |
| Under review | Do not use it yet. We are deciding. |
| Prohibited | Do not use it for company work. |
| Retired | We stopped using it. The row stays for our records. |

### 7.3 Uses that affect people
If a use affects decisions about people, a qualified person must make the final decision. Write this in the conditions of use. Ask your legal counsel which laws apply in your states and countries. If you have staff or customers in the EU, ask about the EU AI Act rules for high-risk uses.

## 8. Keep the register current

### 8.1 Review schedule

| Risk level | Review at least every |
|---|---|
| Critical and High | 3 months |
| Medium | 6 months |
| Low | 12 months |

The Excel file calculates the next review date.

### 8.2 Review early if
- the vendor changes its model, its terms, or its owner
- the tool starts to see a higher data tier
- people outside the company start to see the output or talk to the tool
- an agent gets new permissions
- an incident or a near miss happens
- a new law applies to the use

### 8.3 Find the tools that are not in the register
Every [3] months, ask each team which AI tools they use. Also check the AI features that your existing software added since the last check. Add each new use with the status "Under review".

### 8.4 Retire a tool
1. Remove the accounts and the connections. Revoke the API keys.
2. Export the data that you must keep.
3. Ask the vendor to delete our data. Keep the confirmation.
4. Change the status to "Retired" and write the date.

### 8.5 Change log
Record every change to the register in the "Change log" sheet: the date, the ID, the change, and who made it.

---

## Appendix A. Framework mapping

This table shows which parts of common AI frameworks each section supports. Use it when auditors or customers ask how your register aligns with these frameworks. Alignment with a framework does not mean legal compliance.

| Section | [NIST AI RMF 1.0](https://www.nist.gov/itl/ai-risk-management-framework) | [NIST AI 600-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf) (Generative AI Profile) | [ISO/IEC 42001:2023](https://www.iso.org/standard/42001), Annex A areas | [EU AI Act](https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng) (if you have customers or staff in the EU) |
|---|---|---|---|---|
| 1–2 The register and what goes in it | [GOVERN 1.6](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=28) | [GV-1.6-001](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=20), [GV-1.6-002](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=20), [GV-6.1-007](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=25) | A.4 Resources for AI systems; A.10 Third-party and customer relationships | — |
| 3 Roles | [GOVERN 2.1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=28) | — | A.3 Internal organization | — |
| 5 The columns | [MAP 1.1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=31), [MAP 4.1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=32) | [GV-1.6-003](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=20) | A.6 AI system life cycle; A.7 Data for AI systems | — |
| 6 Risk scoring | [MAP 5.1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=32), [MANAGE 1.2](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=37) | [GV-1.3-001](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=18) | A.5 Assessing impacts of AI systems | [Article 6](https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng#art_6) and [Annex III](https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng#anx_III) (which uses are high-risk) |
| 7 Decisions | [MANAGE 1.1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=37), [MANAGE 1.3](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=37), [MANAGE 1.4](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=37) | [GV-1.3-002](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=18) | A.9 Use of AI systems | [Article 26](https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng#art_26) (duties of companies that use high-risk AI) |
| 8.1–8.3 Reviews | [GOVERN 1.5](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=28), [MEASURE 3.1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=35), [MANAGE 3.1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=37) | [MG-1.3-002](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=44) | A.6 AI system life cycle | — |
| 8.4 Retire a tool | [GOVERN 1.7](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=28) | [GV-1.7-001](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=21), [GV-1.7-002](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=21), [MG-2.4-004](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=46) | A.6 AI system life cycle | — |

**Notes.** We checked the NIST references against [NIST AI 100-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf) and [NIST AI 600-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf). MANAGE 1.3 names the 4 ways to respond to a risk: mitigate, transfer, avoid, or accept. The [ISO/IEC 42001](https://www.iso.org/standard/42001) areas come from public summaries, so check them against the standard before an audit. The risks in section 6.1 match the [OWASP Top 10 for LLM Applications 2026](https://genai.owasp.org/resource/owasp-genai-llm-top-10-2026/). The matching items are LLM01 Prompt Injection, LLM02 Sensitive Information Disclosure, LLM03 Excessive Agency, LLM04 Supply Chain, and LLM07 Misinformation. Frameworks and laws change. This mapping is current as of [November 2026].

---
*Template by [NosisTech LLC](https://nosistech.com). Part of the free [governance-templates](https://github.com/nosistech/governance-templates) collection. Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).*
