# AI Tool Register Guide: Keystone Advisory (fictional example)

> **This is a fictional worked example.** Keystone Advisory does not exist. Any resemblance to a real company is a coincidence. It shows how a small consulting firm could adapt the [generic AI Tool Register](../generic/ai-tool-register-guide.md). Ask your legal counsel to review your own register process. This example is not legal advice.
>
> Open to use and adapt under the license.

| Document control | |
|---|---|
| Company | Keystone Advisory: a remote consulting firm with 12 consultants. It advises mid-size companies on operations, finance, and technology. |
| Register owner | Operations Manager |
| Approved by | Managing Partner |
| Effective date | November 1, 2026 |
| Version | 1.0 |
| Next review of this guide | October 31, 2027 |

---

## 1. Purpose

The AI Tool Register is the list of every AI tool that Keystone uses, with a risk score for each use. It answers 4 questions:

1. Which AI tools do we use, and for what?
2. Who is responsible for each one?
3. How risky is each use?
4. Is each use approved, approved with conditions, or not allowed?

Our AI Acceptable-Use Policy tells consultants to use only approved tools. This register is where we write down "approved". It is also the source for the tool table in our [client AI-use notice](../../01-ai-acceptable-use-policy/consulting-firm/client-ai-use-notice.md). When a client asks "which AI do you use on our work?", this register is the answer.

## 2. What goes in the register

### 2.1 One row for each use, not for each vendor
The same tool can be safe for one task and risky for another. A chat assistant that drafts our own proposals is lower risk. The same chat assistant that analyzes a client's financial data is higher risk. Give each use its own row.

### 2.2 Include all of these
- the business chat assistant and the research tools that Keystone pays for
- AI features inside our office suite, CRM, and proposal software
- meeting notetakers
- browser extensions and AI browsers
- AI agents and AI tools connected to our email, files, or calendar
- personal AI accounts, with the status "Prohibited", so that the decision is on record

### 2.3 What we do not register
Spell check and grammar suggestions that do not send text outside the software. If you are not sure, ask the Operations Manager.

## 3. Roles

| Role | Who | Responsibilities |
|---|---|---|
| Register owner | Operations Manager | Keeps the register complete and current. Sets up tools and accounts. Removes access when people leave. |
| Policy owner | Managing Partner | Approves tools and exceptions. Approves Medium and High uses. |
| Partners | All partners | Decide together on Critical uses |
| Tool owner | One named consultant for each row | Knows how the tool is used. Keeps the row correct. Can switch the tool off. |
| Engagement lead | The partner who leads each engagement | Gets the client AI choice before work starts. Checks that the team uses only tools that the choice allows. |
| All consultants | Everyone | Ask before you use a new tool or a new use. Report AI tools that are not in the register. |

## 4. How a new use gets into the register

1. A consultant fills in the AI Tool Request Form and emails it to the Managing Partner.
2. The Operations Manager adds a row with the status "Under review".
3. The Operations Manager and the tool owner score the risk (section 6).
4. The approver for that risk level decides (section 7).
5. The Operations Manager records the decision, the conditions, the approver, and the date.
6. The Operations Manager tells the consultant who asked. We decide within 5 business days.
7. If the new tool will process client data, the engagement lead tells each affected client first. The Operations Manager updates the client AI-use notice.

## 5. The columns

The Excel file has the same columns as the [generic register](../generic/ai-tool-register-guide.md). Keystone adds these rules:

| Column | Keystone rule |
|---|---|
| Highest data tier | All client data is Restricted. Our own proposals, templates, and methods are Internal. |
| Vendor terms: no training on our data? | "Yes" only if the contract says that the vendor does not train on our data. The contract must also say when the vendor deletes it. |
| Conditions of use | Write the client AI choice limits here, for example "Only for clients that agreed" or "Public data only". Also write "one workspace per client" for every tool that sees client data. |
| Tool owner | A named consultant, not "everyone" |

## 6. How to score the risk

### 6.1 Ask "what could go wrong?"
For each use, write down the worst thing that could credibly happen. Use these common AI risks as a checklist:

- **Data leaks:** the tool exposes a client's confidential information.
- **Mixed clients:** one client's data appears in work for another client.
- **Wrong output:** the tool invents facts, sources, or numbers, and a client relies on them.
- **Hidden instructions:** a website or a client document tells the AI tool to do something harmful. Experts call this "prompt injection".
- **Too much power:** an agent sends an email or shares a file that nobody approved.
- **Vendor problems:** the vendor changes its terms, its model, or its prices, or it has a breach.

### 6.2 Likelihood: how probable is the harm in the next 12 months?

| Score | Name | Meaning |
|---|---|---|
| 1 | Rare | We do not expect it in the next 12 months. |
| 2 | Unlikely | It could happen once in several years. |
| 3 | Possible | It could happen about once a year. |
| 4 | Likely | It could happen several times a year. |
| 5 | Almost certain | It happens every month, or it already happened here. |

Score the chance that the harm reaches a client, not the chance of a small error. A consultant who checks the output stops most errors.

### 6.3 Impact: how bad is the worst credible case?

| Score | Name | Meaning at Keystone |
|---|---|---|
| 1 | Negligible | A small fix that nobody outside the team notices |
| 2 | Minor | Internal rework on our own documents |
| 3 | Moderate | An error in a client deliverable that we find and correct |
| 4 | Major | A client's confidential information is exposed, or a client relies on a wrong number or a false source |
| 5 | Severe | We lose several clients, or a client claims damages from us |

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
3. If the tool sees client data, the impact is at least 4.
4. If the tool sees client data and the vendor terms are "Unknown", the status is "Under review" until we check the contract.
5. The Operations Manager and the Managing Partner score each High or Critical use together.

## 7. Decisions

### 7.1 Who decides

| Risk level | Who approves | What the approver does |
|---|---|---|
| Low | Operations Manager | Approves with the standard rules in our AI Acceptable-Use Policy |
| Medium | Managing Partner | Approves with written conditions of use |
| High | Managing Partner | Approves only with conditions and a written plan to lower the score |
| Critical | Nobody, until the score goes down | Change the use or add controls until the score is 15 or lower. Only the partners together can accept a Critical risk, in writing, for a limited time. |

### 7.2 Status

| Status | Meaning |
|---|---|
| Approved | Consultants can use the tool for this use, under our AI Acceptable-Use Policy. |
| Approved with conditions | Consultants can use it, but only under the conditions in the row and the client AI choice. |
| Under review | Do not use it yet. We are deciding. |
| Prohibited | Do not use it for Keystone work. |
| Retired | We stopped using it. The row stays for our records. |

### 7.3 The client AI choice comes first
An approved tool is not approved for every client. Before you use a tool on client data, check two things:

1. The register approves the tool for Restricted data.
2. The client AI choice allows it. The engagement lead keeps the signed choice in the engagement folder.

If the client did not agree, use AI tools only on public information for that engagement.

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
- the tool starts to see client data for the first time
- a client changes its AI choice, or a new contract has AI terms
- an agent gets new permissions
- an incident or a near miss happens
- a new law applies to the use

### 8.3 Find the tools that are not in the register
Every 3 months, the Operations Manager asks each consultant which AI tools they use. The Operations Manager also checks the AI features that our office software added since the last check. Each new use gets a row with the status "Under review".

### 8.4 Retire a tool
1. Remove the accounts and the connections. Revoke the API keys.
2. Move the deliverables that we must keep to the engagement folders.
3. Ask the vendor to delete our data and our clients' data. Keep the confirmation.
4. Change the status to "Retired" and write the date.
5. Update the client AI-use notice, and tell the affected clients.

### 8.5 Change log
Record every change to the register in the "Change log" sheet: the date, the ID, the change, and who made it.

---

## Appendix A. Security risks

The risks in section 6.1 match the [OWASP Top 10 for LLM Applications 2026](https://genai.owasp.org/resource/owasp-genai-llm-top-10-2026/).

The matching items are LLM01 Prompt Injection, LLM02 Sensitive Information Disclosure, and LLM03 Excessive Agency.

They also include LLM04 Supply Chain and LLM07 Misinformation.

There are four ways to respond to a risk: mitigate, transfer, avoid, or accept.

If your firm works with lawyers, also read [ABA Formal Opinion 512](https://www.americanbar.org/content/dam/aba/administrative/professional_responsibility/ethics-opinions/aba-formal-opinion-512.pdf) on generative AI tools.

Laws and guidance change. This note is current as of November 2026.

---
*Template by [NosisTech LLC](https://nosistech.com). Part of the [governance-templates](https://github.com/nosistech/governance-templates) collection. Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).*
