# AI Vendor Review Guide: Lumorra Data, Inc. (fictional example)

> **This is a fictional worked example.** Lumorra Data, Inc. does not exist. Any resemblance to a real company is a coincidence. It shows how a software company that builds on AI model providers could adapt the [generic template](../generic/ai-vendor-review-guide.md). Ask your legal counsel to review your own process. This example is not legal advice.
>
> Open to use and adapt under the license.

| Document control | |
|---|---|
| Company | Lumorra Data, Inc.: a multi-tenant AI platform that lets mid-size companies search, summarize, and automate work on their own documents. About 45 staff, remote-first, customers in the US and the EU. |
| Review owner | Head of Security and Compliance |
| Approved by | Chief Executive Officer and Chief Technology Officer |
| Effective date | November 1, 2026 |
| Version | 1.0 |
| Next review of this guide | October 31, 2027 |

---

## 1. Purpose

Lumorra buys AI in two ways. Our staff use AI tools to do their work. Our product sends customer content to AI model providers. This guide covers both kinds of vendor. It answers 4 questions:

1. What does the vendor do with our data and with our customers' content?
2. How does the vendor protect it, and what happens when something goes wrong?
3. Can we control the AI, check its output, and switch it off?
4. Can we leave, and take our data with us?

Our customer contracts make promises about the AI in our product, for example no training and limits on retention. A model provider must let us keep those promises. This review checks that it does.

This review feeds the Lumorra AI Tool Register. The register records the decision. This review records the reasons.

## 2. When to review a vendor

Review the vendor:

- before we approve a new AI tool or a new AI feature at the Standard or Deep tier (section 5)
- before we add a new model provider, or a new model from an existing provider, to the product
- before a tool starts to see customer content, or other data of a higher tier than before
- when the vendor changes its model, its data terms, its sub-processors, or its owner
- after the vendor has a breach or a serious AI incident
- before we renew the contract, if the last review is older than the review interval (section 10)

A tool at the Light tier needs only the Light questions. The review owner can do that review alone.

## 3. Roles

| Role | Who | Responsibilities |
|---|---|---|
| Review owner | Head of Security and Compliance | Runs the review. Sends the questions. Judges the security and data answers. |
| Requester | The engineer or the team lead who asked for the tool or the model | Explains the use. Answers the triage. Helps to judge the technical answers. |
| CTO | Chief Technology Officer | Judges the answers about models, model changes, and usage limits |
| Privacy counsel | [Privacy counsel] | Checks the DPA, the sub-processor terms, and the flow-down to our customer contracts |
| Approver | The AI Review Group, for every model provider in the product | Decides, based on the review |

## 4. The review in 7 steps

1. The requester and the review owner answer the 6 triage questions in the Excel file. The file chooses the tier.
2. The review owner sends the questions for that tier to the vendor, with a deadline of 10 business days.
3. The review owner copies the answers and the names of the evidence documents into the Excel file.
4. The review owner, the requester, and the CTO give each answer a status (section 7).
5. The review owner sends follow-up questions for every "Follow-up" answer.
6. The approver decides (section 9).
7. The review owner records the decision in the AI Tool Register and files the Excel file with the evidence.

## 5. Choose the tier

Not every tool needs every question. A tool that checks the grammar of our blog does not need the same review as the model that answers questions about customer documents. The triage sets the tier:

| Triage question | If yes, the tier is at least |
|---|---|
| T1. Will the tool see Internal data, for example internal emails, drafts, or plans? | Standard |
| T2. Will the tool see Restricted data, for example customer content, personal data, credentials, or source code? | Deep |
| T3. Will our customers, their users, or the public see the output or talk to the tool? For every model provider in our product, the answer is Yes. | Deep |
| T4. Will the output help to decide about people, for example hiring, pay, credit, health care, housing, insurance, or education? | Deep |
| T5. Can the tool take actions or connect to our systems, for example send messages, change records, or read our files? | Deep |
| T6. Would an outage of the tool stop important work? | Standard |

| Tier | Questions to send | Typical example at Lumorra |
|---|---|---|
| Light | 6 | A writing tool for the public blog |
| Standard | 27 | A chat assistant on a business plan that sees internal plans |
| Deep | 47 | A model provider behind a feature in our product, or a code assistant that sees our source code |

The Deep tier includes the 5 model provider questions in section K. Every model provider in our product is Deep. If you are not sure about a triage answer, answer "Yes".

## 6. Deal-breakers

Some answers stop the approval as planned. In the Excel file, these questions show "Yes" in the Deal-breaker column. If the answer to one of them is "Not acceptable", we do not approve the use as planned:

1. **B1. Training on our data.** The vendor or its model providers train AI models on our data or our customers' content, and we cannot switch it off.
2. **B6. Sub-processors.** The vendor does not name the sub-processors that receive our data, including AI model providers.
3. **B7. Deletion.** The vendor cannot delete our data, or cannot confirm the deletion.
4. **G2. Incident notice.** The vendor does not commit to tell us about incidents in time for the notice that our customer contracts promise.
5. **H1. Data processing agreement.** The vendor does not offer or sign a data processing agreement, and the tool sees personal data.
6. **H2. Regulated data.** The vendor does not sign the agreements that our laws or our customers require for regulated data.
7. **F3. Approval of actions.** The AI can take actions that are difficult to undo, and we cannot require a person's approval first.
8. **F4. Switch-off.** We cannot switch off the AI feature, the agent, or the model quickly.
9. **K1. Retention.** For a model provider in our product: the provider cannot meet the retention limits that our customer contracts promise.

A failed deal-breaker does not always end the conversation. You can approve a smaller use instead, for example for internal content only. Run the triage again for the smaller use.

## 7. Judge the answers

### 7.1 Status for each answer

| Status | Meaning |
|---|---|
| Acceptable | The answer meets our needs for this use. |
| Follow-up | The answer is missing, unclear, or needs a document. We ask again. |
| Not acceptable | The answer does not meet our needs for this use. |
| Not applicable | The question does not apply to this tool. Write the reason in the notes. |

### 7.2 Rules for judging
1. Judge each answer against our use, not in general. A long retention period can be acceptable for public data and not acceptable for customer content.
2. A missing answer is "Follow-up", never "Acceptable".
3. For each deal-breaker, the answer must point to a contract, the vendor's terms, or an independent report. A sales email or a marketing page is not enough.
4. If the vendor's answer and its contract disagree, the contract counts.
5. "We do not train on your data" does not mean "we do not keep your data". Read the answers to B1, B4, and K1 together.
6. If the vendor uses another company's AI model, ask the same data questions about that company.
7. For a model provider in our product, compare each answer with our customer contracts and our public sub-processor list. Our promise to customers sets the bar.

## 8. The model provider questions (section K)

These questions apply only to model providers in our product.

| Question | Why we ask |
|---|---|
| K1. Zero retention | Our customer contracts limit how long anyone keeps customer content. Many providers keep data for a period to detect abuse, unless a zero-retention option applies. |
| K2. Regional processing | Some EU customers require processing in the EU. We must know which models run where. |
| K3. Model retirement notice | We give customers notice before a model change. The provider's notice must be longer than ours. |
| K4. Spending and rate limits | A bug or an attack can send a huge number of requests. Limits stop the bill and the outage. This addresses LLM06 Unbounded Consumption. |
| K5. Sub-processor list and flow-down | We must list the provider as a sub-processor, and pass its data commitments on to our customers. |

The CTO judges K3 and K4. The review owner and privacy counsel judge K1, K2, and K5.

After approval, we follow the steps for a new model provider in our AI Tool Register guide. We add the provider to our public sub-processor list, and we give customers the notice that their contracts require.

## 9. Decide and record

The Summary sheet in the Excel file counts the statuses and shows one of these results:

| Result | What to do |
|---|---|
| Wait: answers missing or follow-up open | Finish the follow-up first. |
| Decide: some answers are not acceptable | The approver decides. Approve with conditions, approve a smaller use, or do not approve. |
| Do not approve as planned: a deal-breaker failed | Do not approve this use. Consider a smaller use, or another vendor. |
| Ready to decide: record the decision in the AI Tool Register | The approver decides and records the conditions. |

Then record the review in the AI Tool Register:

1. Set "Vendor terms: no training on our data?" from the answers to B1 and B2.
2. Write the conditions that came from the review in "Conditions of use", for example "Zero retention on" or "EU customers on EU models only".
3. Use the risk score in the register to choose the approver. A model provider in the product uses an "AI-P" row.
4. Send the contract terms that need changes to privacy counsel.
5. File the Excel file and the evidence in the security and compliance folder.

## 10. Review the vendor again

| Tier | Review the vendor again at least every |
|---|---|
| Deep | 12 months |
| Standard | 24 months, or at contract renewal if sooner |
| Light | At contract renewal |

Review early if:

- the vendor changes the model that a feature uses, or announces a model retirement
- the vendor changes its data terms, its sub-processors, its regions, or its owner
- the vendor has a breach or a serious AI incident
- we start to use the tool with customer content, or for a new use
- the tool gets new actions or new connections to our systems

A change of model or model version is a product change. It follows the same steps as a new model.

## 11. Keep the evidence

For each review, keep:

- the completed Excel file
- the vendor's documents, for example the contract, the DPA, the security report, and the system card
- the follow-up emails
- the decision and the approver's name

Keep them for the length of the contract plus 3 years. Customers and auditors often ask for them.

## 12. Worked example: a model provider for the product

The Excel file in this folder shows a review in progress. The vendor is an example: "[Model provider]". Its model answers questions about customer documents in the Lumorra platform.

- **Triage:** T1, T2, T3, and T6 are "Yes". The tier is Deep.
- **First round of answers:** the file holds the vendor's answers to the deal-breakers and the model provider questions.
- **What passed:** no training in the agreement (B1), zero retention with written exclusions (K1), and 72-hour incident notice (G2). Six months' notice before a model retires (K3) and spending limits (K4) also passed.
- **What needs follow-up:** two newer models run only in the US, and EU processing is on a web page, not in the agreement (K2).
- **Conditions of use:** zero retention on, no stored files or batch feature for customer content, and EU customers on EU models only.
- **Result:** "Wait". The review owner sends one follow-up email and fills in the remaining answers.

---

## Appendix A. Security risks

The questions cover risks from the [OWASP Top 10 for LLM Applications 2026](https://genai.owasp.org/resource/owasp-genai-llm-top-10-2026/).

The matching items are LLM01 Prompt Injection (C3), LLM02 Sensitive Information Disclosure (section B), and LLM03 Excessive Agency (section F).

They also include LLM04 Supply Chain (section D). Question K4 addresses LLM06 Unbounded Consumption.

Laws and guidance change. This note is current as of November 2026.

---
*Fictional example by [NosisTech LLC](https://nosistech.com). Part of the [governance-templates](https://github.com/nosistech/governance-templates) collection. Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).*
