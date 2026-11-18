# AI Vendor Review: Guide (template)

> **How to use this template.** This guide explains how to review an AI vendor before you approve its tool. The questions are in the Excel file and in the vendor questionnaire, both in the same folder. Replace every item in `[square brackets]`. Delete the parts that do not apply to you. This template is not legal advice.
>
> Open to use and adapt under the license.

| Document control | |
|---|---|
| Company | [Company Name] |
| Review owner | [Name, title] |
| Approved by | [Name, title] |
| Effective date | [Date] |
| Version | [1.0] |
| Next review of this guide | [Date, at most 12 months after the effective date] |

---

## 1. Purpose

Before an AI tool sees our data, we want to know what the vendor does with it. This guide sets out how we ask, how we judge the answers, and how we decide. It answers 4 questions:

1. What does the vendor do with our data?
2. How does the vendor protect it, and what happens when something goes wrong?
3. Can we control the AI, check its output, and switch it off?
4. Can we leave, and take our data with us?

This review feeds our AI Tool Register. The register records the decision. This review records the reasons.

## 2. When to review a vendor

Review the vendor:

- before we approve a new AI tool or a new AI feature at the Standard or Deep tier (section 5)
- before a tool starts to see a higher data tier than before
- when the vendor changes its model, its data terms, or its owner
- after the vendor has a breach or a serious AI incident
- before we renew the contract, if the last review is older than the review interval (section 9)

A tool at the Light tier needs only the Light questions. The review owner can do that review alone.

## 3. Roles

| Role | Who | Responsibilities |
|---|---|---|
| Review owner | [Name, title] | Runs the review. Sends the questions. Judges the answers with the requester. |
| Requester | The person who asked for the tool | Explains the use. Answers the triage. Helps to judge the answers. |
| Vendor contact | A named person at the vendor | Answers the questions and sends the evidence |
| Approver | Depends on the risk level in the AI Tool Register | Decides, based on the review |
| Legal counsel | [Name or firm] | Reviews the contract terms that the review flags |

## 4. The review in 7 steps

1. The requester and the review owner answer the 6 triage questions in the Excel file. The file chooses the tier.
2. The review owner sends the questions for that tier to the vendor, with a deadline of [10] business days.
3. The review owner copies the answers and the names of the evidence documents into the Excel file.
4. The review owner and the requester give each answer a status (section 7).
5. The review owner sends follow-up questions for every "Follow-up" answer.
6. The approver decides (section 8).
7. The review owner records the decision in the AI Tool Register and files the Excel file with the evidence.

## 5. Choose the tier

Not every tool needs every question. A tool that rewrites public web text does not need the same review as a tool that reads customer records. The triage sets the tier:

| Triage question | If yes, the tier is at least |
|---|---|
| T1. Will the tool see Internal data, for example internal emails, drafts, or plans? | Standard |
| T2. Will the tool see Restricted data, for example personal data, customer data, financial data, or health data? | Deep |
| T3. Will customers, patients, or the public see the output or talk to the tool? | Deep |
| T4. Will the output help to decide about people, for example hiring, pay, credit, health care, housing, insurance, or education? | Deep |
| T5. Can the tool take actions or connect to our systems, for example send messages, change records, or read our files? | Deep |
| T6. Would an outage of the tool stop important work? | Standard |

| Tier | Questions to send | Typical example |
|---|---|---|
| Light | 6 | A writing tool that sees only public information |
| Standard | 27 | A chat assistant on a business plan that sees internal drafts |
| Deep | 42 | A support chatbot that reads customer records and answers customers |

If you are not sure about a triage answer, answer "Yes".

## 6. Deal-breakers

Some answers stop the approval as planned. In the Excel file, these questions show "Yes" in the Deal-breaker column. If the answer to one of them is "Not acceptable", we do not approve the use as planned:

1. **B1. Training on our data.** The vendor or its model providers train AI models on our data, and we cannot switch it off.
2. **B6. Sub-processors.** The vendor does not name the sub-processors that receive our data, including AI model providers.
3. **B7. Deletion.** The vendor cannot delete our data, or cannot confirm the deletion.
4. **G2. Incident notice.** The vendor does not commit to tell us about incidents that affect our data or our users.
5. **H1. Data processing agreement.** The vendor does not offer or sign a data processing agreement, and the tool sees personal data.
6. **H2. Regulated data.** The vendor does not sign the agreements that our laws require for regulated data, for example a Business Associate Agreement for US health data.
7. **F3. Approval of actions.** The AI can take actions that are difficult to undo, and we cannot require a person's approval first.
8. **F4. Switch-off.** We cannot switch off the AI feature or an agent quickly.

A failed deal-breaker does not always end the conversation. You can approve a smaller use instead, for example without Restricted data. Run the triage again for the smaller use.

## 7. Judge the answers

### 7.1 Status for each answer

| Status | Meaning |
|---|---|
| Acceptable | The answer meets our needs for this use. |
| Follow-up | The answer is missing, unclear, or needs a document. We ask again. |
| Not acceptable | The answer does not meet our needs for this use. |
| Not applicable | The question does not apply to this tool. Write the reason in the notes. |

### 7.2 Rules for judging
1. Judge each answer against our use, not in general. A long retention period can be acceptable for public data and not acceptable for customer data.
2. A missing answer is "Follow-up", never "Acceptable".
3. For each deal-breaker, the answer must point to a contract, the vendor's terms, or an independent report. A sales email or a marketing page is not enough.
4. If the vendor's answer and its contract disagree, the contract counts.
5. "We do not train on your data" does not mean "we do not keep your data". Read the answers to B1 and B4 together.
6. If the vendor uses another company's AI model, ask the same data questions about that company.

## 8. Decide and record

The Summary sheet in the Excel file counts the statuses and shows one of these results:

| Result | What to do |
|---|---|
| Wait: answers missing or follow-up open | Finish the follow-up first. |
| Decide: some answers are not acceptable | The approver decides. Approve with conditions, approve a smaller use, or do not approve. |
| Do not approve as planned: a deal-breaker failed | Do not approve this use. Consider a smaller use, or another vendor. |
| Ready to decide: record the decision in the AI Tool Register | The approver decides and records the conditions. |

Then record the review in the AI Tool Register:

1. Set "Vendor terms: no training on our data?" from the answers to B1 and B2.
2. Write the conditions that came from the review in "Conditions of use", for example "No Restricted data" or "Feedback buttons switched off".
3. Use the risk score in the register to choose the approver.
4. Send the contract terms that need changes to legal counsel.
5. File the Excel file and the evidence in [location].

## 9. Review the vendor again

| Tier | Review the vendor again at least every |
|---|---|
| Deep | 12 months |
| Standard | 24 months, or at contract renewal if sooner |
| Light | At contract renewal |

Review early if:

- the vendor changes the model that a feature uses
- the vendor changes its data terms, its sub-processors, or its owner
- the vendor has a breach or a serious AI incident
- we start to use the tool with a higher data tier, or for a new use
- the tool gets new actions or new connections to our systems

## 10. Keep the evidence

For each review, keep:

- the completed Excel file
- the vendor's documents, for example the contract, the terms, the security report, and the system card
- the follow-up emails
- the decision and the approver's name

Keep them for [the length of the contract plus 3 years].

---

## Appendix A. Security risks

The questions cover risks from the [OWASP Top 10 for LLM Applications 2026](https://genai.owasp.org/resource/owasp-genai-llm-top-10-2026/).

The matching items are LLM01 Prompt Injection (C3), LLM02 Sensitive Information Disclosure (section B), and LLM03 Excessive Agency (section F).

They also include LLM04 Supply Chain (section D).

Laws and guidance change. This note is current as of [November 2026].

---
*Template by [NosisTech LLC](https://nosistech.com). Part of the [governance-templates](https://github.com/nosistech/governance-templates) collection. Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).*
