# AI Tool Register Guide: Lumorra Data, Inc. (fictional example)

> **This is a fictional worked example.** Lumorra Data, Inc. does not exist. Any resemblance to a real company is a coincidence. It shows how a B2B software company that builds an AI product could adapt the [generic template](../generic/ai-tool-register-guide.md). Ask your legal counsel to review your own register process. This example is not legal advice.
>
> Free to use and adapt.

| Document control | |
|---|---|
| Company | Lumorra Data, Inc.: a multi-tenant AI platform that lets mid-size companies search, summarize, and automate work on their own documents. About 45 staff, remote-first, customers in the US and the EU. |
| Register owner | Head of Security and Compliance |
| Approved by | Chief Executive Officer and Chief Technology Officer |
| Effective date | November 1, 2026 |
| Version | 1.0 |
| Next review of this guide | October 31, 2027 |

---

## 1. Purpose

The Lumorra AI Tool Register is the list of every AI use at Lumorra Data, with a risk score for each use. It answers 4 questions:

1. Which AI tools and AI features do we use, and for what?
2. Who is responsible for each one?
3. How risky is each use?
4. Is each use approved, approved with conditions, or not allowed?

Our AI Acceptable-Use Policy tells staff to use only approved tools. This register is where we write down "approved". Enterprise customers ask about our AI in most security reviews. This register gives the answer, and Appendix A shows how to use it.

## 2. What goes in the register

### 2.1 Two kinds of rows
Lumorra uses AI in two ways, so the register has two kinds of rows:

| Kind of row | What it covers | Example |
|---|---|---|
| **Staff tools** | AI tools that our staff use to do their work | A code assistant that our engineers use |
| **Product AI** | Each model provider and each AI feature inside the Lumorra platform | The model that answers questions about a customer's documents |

Product AI rows matter most. They process customer data, and our customer contracts make promises about them.

### 2.2 One row for each use, not for each vendor
The same model provider can power two features with different risks. A feature that summarizes one document is lower risk. An agent that can change records in a customer's systems is higher risk. Give each use its own row.

### 2.3 Include all of these
- chat assistants, code assistants, and AI agents that staff use
- MCP servers, plugins, and IDE extensions. MCP (Model Context Protocol) servers are connectors that give an AI tool access to other software or data. Each one counts as a tool.
- AI features inside our business software, for example email, documents, CRM, and the help desk
- meeting recorders and AI notetakers
- each model provider that our product calls through an API
- each AI feature in the Lumorra platform, including agents and search
- free or personal AI accounts, with the status "Prohibited", so that the decision is on record

### 2.4 What we do not register
We do not register spell check and grammar suggestions that do not send data outside the software. If you are not sure, register the feature.

## 3. Roles

| Role | Who | Responsibilities |
|---|---|---|
| Register owner | Head of Security and Compliance | Keeps the register complete and current. Runs the reviews. Reports to the CEO and the CTO. |
| AI Review Group | Head of Security and Compliance, CTO, Head of Product, privacy counsel | Approves High uses, new model providers, and new AI features in the product |
| Tool owner | One named person for each staff tool and each AI feature | Knows how the tool or feature is used. Keeps the row correct. Can switch it off. |
| Engineering leads | All team leads | Tell the register owner about each new AI library, model, or connector in their team's work |
| All staff | Everyone | Ask before you use a new tool or a new use. Report AI tools that are not in the register. |

## 4. How a new use gets into the register

1. A person opens a ticket in the security queue with the AI Tool Request Form.
2. The register owner adds a row with the status "Under review".
3. The register owner and the tool owner score the risk (section 6).
4. The approver for that risk level decides (section 7).
5. The register owner records the decision, the conditions, the approver, and the date.
6. The register owner closes the ticket and tells the person who asked. We decide within 5 business days.

### 4.1 Extra steps for a new model provider
A new model provider needs approval from the AI Review Group. Before it processes customer data, we complete these steps:

1. The provider agrees in its contract not to train on customer data. It also meets our retention limits.
2. We add the provider to our public sub-processor list.
3. We give customers the notice that their contracts require.

### 4.2 Extra steps for a new AI feature in the product
Before we release an AI feature, we run our evaluation and security tests. The tests cover prompt injection, data leakage, and unsafe agent actions. The Secure Development Standard gives the detailed steps. The register row links to the latest test results.

## 5. The columns

| Column | What to write | Example |
|---|---|---|
| ID | A unique number. Product AI rows start with "AI-P". | AI-P01 |
| Tool and plan | The product name and the plan. The plan matters: free and business plans often have different data terms. | [Code assistant], business plan |
| Vendor | The company that provides the tool or the model | Model provider A |
| What we use it for | The task, in one sentence | Answer user questions about the customer's own documents |
| Type of AI | Choose from the list. Use "AI in a product we sell" for product AI rows. | AI in a product we sell |
| Tool owner | One named person | Head of Product |
| Who uses it | Teams and approximate number of people, or the customers who use the feature | All customers, about [300] tenants |
| Highest data tier | The most sensitive data that the tool sees: Public, Internal, or Restricted. All customer data is Restricted. | Restricted |
| Affects decisions about people? | Yes, if the output helps to decide about hiring, pay, credit, health care, housing, insurance, or education | No |
| Human check | How a person checks the output | Person monitors and can stop it |
| Vendor terms: no training on our data? | Yes, No, or Unknown. Check the contract, not the marketing page. | Yes |
| Likelihood | 1 to 5 (section 6) | 2 |
| Impact | 1 to 5 (section 6) | 4 |
| Risk score | Calculated: likelihood × impact | 8 |
| Risk level | Calculated: Low, Medium, High, or Critical | Medium |
| Controls in place | What we do today to lower the risk | Search limited to each tenant's data; tests before each release; feature switch for each tenant |
| Status | Approved, Approved with conditions, Under review, Prohibited, or Retired | Approved with conditions |
| Conditions of use | The rules that apply to this use | Re-test before each model change. Keep the provider on the sub-processor list. |
| Approved by | Name and title | AI Review Group |
| Decision date | The date of the decision | November 2, 2026 |
| Next review | Calculated from the decision date and the risk level | May 2, 2027 |

## 6. How to score the risk

### 6.1 Ask "what could go wrong?"
For each use, write down the worst thing that could credibly happen. Use these common AI risks as a checklist:

- **Data leaks:** the tool exposes our data or our customers' data.
- **Cross-tenant exposure:** one customer's data appears in another customer's results.
- **Wrong output:** the tool invents facts, sources, or numbers, and someone relies on them.
- **Hidden instructions:** a document, a web page, or an email tells the AI to do something harmful. Experts call this "prompt injection".
- **Too much power:** an agent sends, deletes, or changes something that nobody approved.
- **Hidden context exposure:** a user makes the AI reveal its system prompt or other hidden instructions.
- **Runaway cost:** a feature or a user sends so many requests that the cost or the load becomes a problem.
- **Vendor problems:** the model provider changes its terms, its model, or its prices, or it has a breach.

### 6.2 Likelihood: how probable is the harm in the next 12 months?

| Score | Name | Meaning |
|---|---|---|
| 1 | Rare | We do not expect it in the next 12 months. |
| 2 | Unlikely | It could happen once in several years. |
| 3 | Possible | It could happen about once a year. |
| 4 | Likely | It could happen several times a year. |
| 5 | Almost certain | It happens every month, or it already happened here. |

Score the chance that the harm reaches someone, not the chance of a small error.

### 6.3 Impact: how bad is the worst credible case?

| Score | Name | Meaning at Lumorra |
|---|---|---|
| 1 | Negligible | A small fix that nobody outside the team notices |
| 2 | Minor | Internal rework. No customer data and no customer sees it. |
| 3 | Moderate | An error reaches one customer and we correct it quickly |
| 4 | Major | Customer data reaches the wrong person, we break a contract promise, or we lose an important customer |
| 5 | Severe | Data from many customers is exposed, or an event threatens the business |

### 6.4 Calculate the score and the level

**Risk score = likelihood × impact.** The Excel file calculates it for you.

| Score | Risk level |
|---|---|
| 1–4 | Low |
| 5–9 | Medium |
| 10–15 | High |
| 16–25 | Critical |

### 6.5 Scoring rules
1. Score the use as it runs today, with the controls that are really in place. A control that is only planned does not count yet.
2. If you are not sure between two numbers, choose the higher one.
3. If a use processes customer data, the impact is at least 4.
4. If the tool sees Restricted data and the vendor terms are "Unknown", the impact is at least 4.
5. If an agent can take an action that is difficult to reverse without a person's approval, the likelihood is at least 4.
6. Two people score each High or Critical use: the tool owner and the register owner.

## 7. Decisions

### 7.1 Who decides

| Risk level | Who approves | What the approver does |
|---|---|---|
| Low | The tool owner's team lead | Approves with the standard rules in our AI Acceptable-Use Policy |
| Medium | Head of Security and Compliance | Approves with written conditions of use |
| High | AI Review Group | Approves only with conditions and a written plan to lower the score |
| Critical | Nobody, until the score goes down | Change the use or add controls until the score is 15 or lower. Only the CEO can accept a Critical risk, in writing, for a limited time. |

All new model providers and all new AI features in the product go to the AI Review Group, at every risk level.

### 7.2 Status

| Status | Meaning |
|---|---|
| Approved | Staff can use the tool, or the feature can run, for this use. |
| Approved with conditions | The same, but only under the conditions in the row. |
| Under review | Do not use it or release it yet. We are deciding. |
| Prohibited | Do not use it for Lumorra work. |
| Retired | We stopped using it. The row stays for our records. |

### 7.3 Agents
Each agent row must show these controls before approval:

1. The agent has its own credentials, with the minimum access that it needs.
2. A person approves each action that is difficult to reverse, for example a deletion or a message to a customer.
3. We log every action that the agent takes.
4. The tool owner can switch the agent off for one customer or for all customers.

### 7.4 Customers and users in the EU
Some Lumorra customers and their users are in the EU. The EU AI Act asks us to tell people when they interact with an AI system ([Article 50](https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng#art_50)). It also asks companies to support the AI literacy of their staff ([Article 4](https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng#art_4)). The [Digital Omnibus](https://eur-lex.europa.eu/eli/reg/2026/1744/oj/eng) changed several dates in the Act. Our privacy counsel confirms our role and the dates that apply to each AI feature.

## 8. Keep the register current

### 8.1 Review schedule

| Risk level | Review at least every |
|---|---|
| Critical and High | 3 months |
| Medium | 6 months |
| Low | 12 months |

The Excel file calculates the next review date.

### 8.2 Review early if
- a model provider changes the model or the model version that a feature uses
- a vendor changes its terms, its retention, or its owner, or it has a breach
- a feature starts to see a new kind of customer data
- an agent gets new permissions or new connectors
- an incident or a near miss happens
- a customer contract or a new law adds a requirement

A change of model or model version is a product change. It goes through change management and an early review of the row.

### 8.3 Find the tools that are not in the register
Every 3 months, the register owner asks each team lead which AI tools, connectors, and extensions their team uses. The register owner also checks the AI features that our business software added since the last check. Each new use gets a row with the status "Under review".

### 8.4 Retire a tool or a feature
1. Remove the accounts and the connections. Revoke the API keys.
2. Export the data that we must keep.
3. Ask the vendor to delete our data and our customers' data. Keep the confirmation.
4. If the vendor was a model provider, update the sub-processor list.
5. Change the status to "Retired" and write the date.

### 8.5 Change log
Record every change to the register in the "Change log" sheet: the date, the ID, the change, and who made it.

---

## Appendix A. Using the register in customer security reviews

Enterprise customers ask the same AI questions in most security reviews. This table shows where the register answers them.

| Common customer question | Where the register answers it |
|---|---|
| Which AI vendors process our data? | Product AI rows, the Vendor column, and the sub-processor list |
| Do your AI vendors train on our data? | The column "Vendor terms: no training on our data?" |
| How do you decide which AI tools your staff can use? | Sections 4 and 7, and the Status column |
| How do you control AI agents? | Section 7.3, and the conditions of use in each agent row |
| Will you tell us before you change the AI model? | Sections 4.1 and 8.2 |
| How often do you review AI risks? | Section 8.1, and the Next review column |

Send customers an extract of the product AI rows, not the full register. Remove internal notes first.

---

## Appendix B. Framework mapping

This table shows which parts of common AI frameworks each section supports. Use it when auditors or customers ask how your register aligns with these frameworks. Alignment with a framework does not mean legal compliance.

| Section | [NIST AI RMF 1.0](https://www.nist.gov/itl/ai-risk-management-framework) | [NIST AI 600-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf) (Generative AI Profile) | [ISO/IEC 42001:2023](https://www.iso.org/standard/42001), Annex A areas | [EU AI Act](https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng) (customers or staff in the EU) |
|---|---|---|---|---|
| 1–2 The register and what goes in it | [GOVERN 1.6](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=28) | [GV-1.6-001](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=20), [GV-1.6-002](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=20), [GV-6.1-007](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=25) | A.4 Resources for AI systems; A.10 Third-party and customer relationships | — |
| 3 Roles | [GOVERN 2.1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=28) | — | A.3 Internal organization | — |
| 4.1 New model providers | [GOVERN 6.1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=29), [MAP 4.1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=32) | [GV-6.1-007](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=25) | A.10 Third-party and customer relationships | — |
| 5 The columns | [MAP 1.1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=31), [MAP 4.1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=32) | [GV-1.6-003](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=20) | A.6 AI system life cycle; A.7 Data for AI systems | — |
| 6 Risk scoring | [MAP 5.1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=32), [MANAGE 1.2](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=37) | [GV-1.3-001](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=18) | A.5 Assessing impacts of AI systems | [Article 6](https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng#art_6) and [Annex III](https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng#anx_III) (which uses are high-risk) |
| 7 Decisions | [MANAGE 1.1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=37), [MANAGE 1.3](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=37), [MANAGE 1.4](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=37) | [GV-1.3-002](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=18) | A.9 Use of AI systems | [Article 4](https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng#art_4), [Article 50](https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng#art_50) |
| 8.1–8.3 Reviews | [GOVERN 1.5](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=28), [MEASURE 3.1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=35), [MANAGE 3.1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=37) | [MG-1.3-002](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=44) | A.6 AI system life cycle | — |
| 8.4 Retire a tool | [GOVERN 1.7](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf#page=28) | [GV-1.7-001](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=21), [GV-1.7-002](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=21), [MG-2.4-004](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf#page=46) | A.6 AI system life cycle | — |

**Notes.** We checked the NIST references against [NIST AI 100-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf) and [NIST AI 600-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf). The [ISO/IEC 42001](https://www.iso.org/standard/42001) areas come from public summaries, so check them against the standard before an audit. The risks in section 6.1 match the [OWASP Top 10 for LLM Applications 2026](https://genai.owasp.org/resource/owasp-genai-llm-top-10-2026/). The matching items are LLM01 Prompt Injection, LLM02 Sensitive Information Disclosure, LLM03 Excessive Agency, and LLM04 Supply Chain. They also include LLM06 Unbounded Consumption, LLM07 Misinformation, LLM08 Hidden Context Exposure, and LLM09 Vector and Embedding Weaknesses. Frameworks and laws change. This mapping is current as of November 2026.

---
*Fictional example by [NosisTech LLC](https://nosistech.com). Part of the free [governance-templates](https://github.com/nosistech/governance-templates) collection. Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).*
