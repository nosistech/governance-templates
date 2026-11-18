# AI Vendor Review Guide: Keystone Advisory (fictional example)

> **This is a fictional worked example.** Keystone Advisory does not exist. Any resemblance to a real company is a coincidence. It shows how a small consulting firm could adapt the [generic template](../generic/ai-vendor-review-guide.md). Ask your legal counsel to review your own process. This example is not legal advice.
>
> Open to use and adapt under the license.

| Document control | |
|---|---|
| Company | Keystone Advisory: a remote consulting firm with 12 consultants. It advises mid-size companies on operations, finance, and technology. |
| Review owner | Operations Manager |
| Approved by | Managing Partner |
| Effective date | November 1, 2026 |
| Version | 1.0 |
| Next review of this guide | October 31, 2027 |

---

## 1. Purpose

Our clients trust us with their data. Before an AI tool sees it, we want to know what the vendor does with it. This guide sets out how we ask, how we judge the answers, and how we decide. It answers 4 questions:

1. What does the vendor do with our data and our clients' data?
2. How does the vendor protect it, and what happens when something goes wrong?
3. Can we control the AI, check its output, and switch it off?
4. Can we leave, and take our data with us?

This review feeds the Keystone AI Tool Register. The register records the decision. This review records the reasons. Each client's AI choice still decides what we can do on that client's work.

## 2. When to review a vendor

Review the vendor:

- before we approve a new AI tool or a new AI feature at the Standard or Deep tier (section 5)
- before a tool starts to see client data
- when the vendor changes its model, its data terms, its plans, or its owner
- after the vendor has a breach or a serious AI incident
- before we renew the contract, if the last review is older than the review interval (section 10)

A tool at the Light tier needs only the Light questions. The Operations Manager can do that review alone.

## 3. Roles

| Role | Who | Responsibilities |
|---|---|---|
| Review owner | Operations Manager | Runs the review. Sends the questions. Tests the admin settings in a trial account. |
| Requester | The consultant who asked for the tool | Explains the use. Answers the triage. Helps to judge the answers. |
| Approver | Managing Partner, or all partners for a Critical use | Decides, based on the review |
| Engagement leads | The partners who lead engagements | Check that the client AI choice allows the tool before the team uses it on client work |
| Legal counsel | [Law firm] | Reviews the contract terms that the review flags |

## 4. The review in 7 steps

1. The requester and the review owner answer the 6 triage questions in the Excel file. The file chooses the tier.
2. The review owner sends the questions for that tier to the vendor, with a deadline of 10 business days.
3. The review owner copies the answers and the names of the evidence documents into the Excel file.
4. The review owner and the requester give each answer a status (section 7).
5. The review owner sends follow-up questions for every "Follow-up" answer.
6. The approver decides (section 9).
7. The review owner records the decision in the AI Tool Register and files the Excel file with the evidence.

## 5. Choose the tier

Not every tool needs every question. A tool that formats our own slides does not need the same review as a tool that records client calls. The triage sets the tier:

| Triage question | If yes, the tier is at least |
|---|---|
| T1. Will the tool see Internal data, for example our proposals, templates, or methods? | Standard |
| T2. Will the tool see Restricted data, for example any client data, personal data, or secrets? | Deep |
| T3. Will clients or the public see the output or talk to the tool? | Deep |
| T4. Will the output help to decide about people, for example hiring, pay, credit, health care, housing, insurance, or education? | Deep |
| T5. Can the tool take actions or connect to our systems, for example send messages, change records, or read our files? | Deep |
| T6. Would an outage of the tool stop important work? | Standard |

| Tier | Questions to send | Typical example at Keystone |
|---|---|---|
| Light | 6 | A design tool for our public website |
| Standard | 29 | A chat assistant on a business plan that sees our own proposals |
| Deep | 45 | Any tool that sees client data, for example an AI meeting notetaker on client calls |

The Standard tier includes 2 firm control questions (K1, K2). The Deep tier adds the notetaker question (K3). We treat all client data as Restricted, so any tool that sees client data is Deep. If you are not sure about a triage answer, answer "Yes".

## 6. Deal-breakers

Some answers stop the approval as planned. In the Excel file, these questions show "Yes" in the Deal-breaker column. If the answer to one of them is "Not acceptable", we do not approve the use as planned:

1. **B1. Training on our data.** The vendor or its model providers train AI models on our clients' data, and the contract for our plan allows it.
2. **B6. Sub-processors.** The vendor does not name the sub-processors that receive our data, including AI model providers.
3. **B7. Deletion.** The vendor cannot delete our data, or cannot confirm the deletion.
4. **G2. Incident notice.** The vendor does not commit to tell us about incidents that affect our data or our clients.
5. **H1. Data processing agreement.** The vendor does not offer or sign a data processing agreement, and the tool sees personal data.
6. **H2. Regulated data.** The vendor does not sign the agreements that a client's laws require for regulated data, and we plan to use that data.
7. **F3. Approval of actions.** The AI can take actions that are difficult to undo, for example an email to a client, and we cannot require a person's approval first.
8. **F4. Switch-off.** We cannot switch off the AI feature or an agent quickly.

At Keystone, B1 is stricter than in the generic template. A setting that a user can change is not enough. The "no training" promise must be in the contract or the terms for our plan.

A failed deal-breaker does not always end the conversation. You can approve a smaller use instead, for example for our own internal work only. Run the triage again for the smaller use.

## 7. Judge the answers

### 7.1 Status for each answer

| Status | Meaning |
|---|---|
| Acceptable | The answer meets our needs for this use. |
| Follow-up | The answer is missing, unclear, or needs a document. We ask again. |
| Not acceptable | The answer does not meet our needs for this use. |
| Not applicable | The question does not apply to this tool. Write the reason in the notes. |

### 7.2 Rules for judging
1. Judge each answer against our use, not in general. A long retention period can be acceptable for our own templates and not acceptable for client data.
2. A missing answer is "Follow-up", never "Acceptable".
3. For each deal-breaker, the answer must point to a contract, the vendor's terms, or an independent report. A sales email or a marketing page is not enough.
4. If the vendor's answer and its contract disagree, the contract counts.
5. "We do not train on your data" does not mean "we do not keep your data". Read the answers to B1 and B4 together.
6. If the vendor uses another company's AI model, ask the same data questions about that company.
7. Check the plan. No-cost, personal, and business plans of the same product often have different terms. We review the plan that we will buy.

## 8. The firm control questions (section K)

These questions apply only at Keystone.

| Question | Why we ask |
|---|---|
| K1. Admin switches for feedback and sharing | One consultant should not be able to share client data outside the firm by mistake. |
| K2. A separate workspace for each client | Consultants on one engagement should not see another client's work. |
| K3. Meeting notetakers | Notetakers can join calls by themselves and record clients without consent. Some US states require the consent of all parties to record a confidential conversation, for example California ([Penal Code §632](https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?lawCode=PEN&sectionNum=632.)). |

Before we record a client call, the client AI choice must allow it. The consultant also asks each participant at the start of the call.

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
2. Write the conditions that came from the review in "Conditions of use", for example "Automatic join off" or "Ask each participant before you record".
3. Use the risk score in the register to choose the approver.
4. Send the contract terms that need changes to legal counsel.
5. File the Excel file and the evidence in the firm's operations folder.
6. Tell the engagement leads about the decision and the conditions. They check each client AI choice before the team uses the tool.

## 10. Review the vendor again

| Tier | Review the vendor again at least every |
|---|---|
| Deep | 12 months |
| Standard | 24 months, or at contract renewal if sooner |
| Light | At contract renewal |

Review early if:

- the vendor changes the model that a feature uses
- the vendor changes its data terms, its plans, its sub-processors, or its owner
- the vendor has a breach or a serious AI incident
- we start to use the tool with client data, or for a new use
- the tool gets new actions or new connections, for example to our email or our calendars

## 11. Keep the evidence

For each review, keep:

- the completed Excel file
- the vendor's documents, for example the terms, the DPA, and the security report
- the follow-up emails
- the decision and the approver's name

Keep them for the length of the contract plus 3 years. Clients sometimes ask for them.

## 12. Worked example: an AI meeting notetaker

The Excel file in this folder shows a review in progress. The vendor is an example: "[Notetaker vendor]". The notetaker records and summarizes client calls.

- **Triage:** T1, T2, T3, and T5 are "Yes". The tier is Deep.
- **First round of answers:** the file holds the vendor's answers to the deal-breakers and the firm control questions.
- **What passed:** automatic deletion after 30 days (B4), a sub-processor list with countries (B6), and 72-hour incident notice (G2). A workspace for each client (K2) and admin control of summary emails (F3) also passed.
- **What needs follow-up:** the "no training" promise is on a web page, not in the contract (B1). Administrators cannot switch off the feedback buttons (K1).
- **What is not acceptable:** the notetaker does not ask participants for consent (K3).
- **Result:** "Decide". The Managing Partner can approve with a condition: the consultant asks each participant before the notetaker records the call. B1 must still pass before any approval.

---

## Appendix A. Security risks

The questions cover risks from the [OWASP Top 10 for LLM Applications 2026](https://genai.owasp.org/resource/owasp-genai-llm-top-10-2026/).

The matching items are LLM01 Prompt Injection (C3), LLM02 Sensitive Information Disclosure (section B), and LLM03 Excessive Agency (section F).

They also include LLM04 Supply Chain (section D). Recording laws differ by state and country.

Laws and guidance change. This note is current as of November 2026.

---
*Fictional example by [NosisTech LLC](https://nosistech.com). Part of the [governance-templates](https://github.com/nosistech/governance-templates) collection. Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).*
