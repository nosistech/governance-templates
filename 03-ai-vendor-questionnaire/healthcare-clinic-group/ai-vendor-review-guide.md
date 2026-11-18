# AI Vendor Review Guide: Riverbend Family Health (fictional example)

> **This is a fictional worked example.** Riverbend Family Health does not exist. Any resemblance to a real company is a coincidence. It shows how a US outpatient clinic group could adapt the [generic template](../generic/ai-vendor-review-guide.md). Laws change and differ by state. Ask your legal counsel and your HIPAA Privacy Officer to review your own process. This example is not legal advice.
>
> Open to use and adapt under the license.

| Document control | |
|---|---|
| Company | Riverbend Family Health (6 family-medicine clinics: 4 in Texas, 2 in California, about 120 staff) |
| Review owner | Compliance Manager (HIPAA Privacy Officer) |
| Approved by | Chief Executive Officer and Medical Director |
| Effective date | November 1, 2026 |
| Version | 1.0 |
| Next review of this guide | October 31, 2027 |

---

## 1. Purpose

Before an AI tool sees patient information, we want to know what the vendor does with it. This guide sets out how we ask, how we judge the answers, and how we decide. It answers 4 questions:

1. What does the vendor do with our data, and with our patients' data?
2. How does the vendor protect it, and what happens when something goes wrong?
3. Can we control the AI, check its output, and switch it off?
4. Can we leave, and take our data with us?

This review feeds the Riverbend AI Tool Register. The register records the decision. This review records the reasons.

Two terms appear often in this guide:

- **PHI (protected health information):** any information that identifies a patient and relates to their health, their care, or their payment for care.
- **BAA (Business Associate Agreement):** the contract that HIPAA requires before a vendor can create, receive, keep, or send PHI for us.

## 2. When to review a vendor

Review the vendor:

- before we approve a new AI tool or a new AI feature at the Standard or Deep tier (section 5)
- before a tool starts to see PHI, or other data of a higher tier than before
- when the vendor changes its model, its data terms, its subcontractors, or its owner
- after the vendor has a breach or a serious AI incident
- before we renew the contract, if the last review is older than the review interval (section 10)

A tool at the Light tier needs only the Light questions. The review owner can do that review alone.

## 3. Roles

| Role | Who | Responsibilities |
|---|---|---|
| Review owner | Compliance Manager (HIPAA Privacy Officer) | Runs the review. Sends the questions. Checks the BAA and the subcontractors. |
| Requester | The person who asked for the tool | Explains the use. Answers the triage. Helps to judge the answers. |
| HIPAA Security Officer | IT Manager | Judges the security answers. Tests the switch-off and the admin settings in a trial account. |
| Medical Director | Lead physician | Judges the answers about clinical safety, accuracy, and bias. Joins every decision about a clinical tool. |
| Approver | The AI Review Group, for every tool that touches PHI or patient care | Decides, based on the review |
| Legal counsel | [Healthcare law firm] | Reviews the BAA and the contract terms that the review flags |

## 4. The review in 7 steps

1. The requester and the review owner answer the 6 triage questions in the Excel file. The file chooses the tier.
2. The review owner sends the questions for that tier to the vendor, with a deadline of 10 business days.
3. The review owner copies the answers and the names of the evidence documents into the Excel file.
4. The review owner, the requester, and the right specialist give each answer a status (section 7). The Medical Director judges the clinical answers.
5. The review owner sends follow-up questions for every "Follow-up" answer.
6. The AI Review Group decides (section 9).
7. The review owner records the decision in the AI Tool Register and files the Excel file with the evidence.

## 5. Choose the tier

Not every tool needs every question. A tool that rewrites our public web pages does not need the same review as a tool that listens to patient visits. The triage sets the tier:

| Triage question | If yes, the tier is at least |
|---|---|
| T1. Will the tool see Internal data, for example staff emails, schedules, or clinic procedures? | Standard |
| T2. Will the tool see Restricted data, for example PHI, staff records, or payment data? | Deep |
| T3. Will patients or the public see the output or talk to the tool? | Deep |
| T4. Will the output help to decide about patients or staff, for example diagnosis, treatment, triage, or hiring? | Deep |
| T5. Can the tool take actions or connect to our systems, for example write into the EHR, send messages, or book visits? | Deep |
| T6. Would an outage of the tool stop important work? | Standard |

| Tier | Questions to send | Typical example at Riverbend |
|---|---|---|
| Light | 6 | A writing tool for the public website that sees no PHI |
| Standard | 27 | A chat assistant on a business plan that drafts staff training material |
| Deep | 46 | An ambient AI scribe that records visits and writes into the EHR |

The Deep tier includes the 4 patient care questions in section K. Any tool that can see PHI is Deep. If you are not sure about a triage answer, answer "Yes".

## 6. Deal-breakers

Some answers stop the approval as planned. In the Excel file, these questions show "Yes" in the Deal-breaker column. If the answer to one of them is "Not acceptable", we do not approve the use as planned:

1. **B1. Training on our data.** The vendor or its model providers train AI models on our data, and we cannot switch it off.
2. **B6. Sub-processors.** The vendor does not name the sub-processors that receive our data, including AI model providers.
3. **B7. Deletion.** The vendor cannot delete our data, or cannot confirm the deletion.
4. **G2. Incident notice.** The vendor does not commit to tell us about incidents that affect our data or our patients.
5. **H1. Data processing agreement.** The vendor does not offer or sign a data processing agreement, and the tool sees personal data that a BAA does not cover.
6. **H2. BAA.** The vendor does not sign a BAA that covers the AI feature, or a subcontractor that receives PHI has no BAA.
7. **F3. Approval of actions.** The AI can take actions that are difficult to undo, for example a change to the chart, and we cannot require a person's approval first.
8. **F4. Switch-off.** We cannot switch off the AI feature or an agent quickly.
9. **K1. Recording consent.** The product records patient visits, and it gives no way to tell patients, get their consent, or stop the recording.

A failed deal-breaker does not always end the conversation. You can approve a smaller use instead, for example without PHI. Run the triage again for the smaller use.

## 7. Judge the answers

### 7.1 Status for each answer

| Status | Meaning |
|---|---|
| Acceptable | The answer meets our needs for this use. |
| Follow-up | The answer is missing, unclear, or needs a document. We ask again. |
| Not acceptable | The answer does not meet our needs for this use. |
| Not applicable | The question does not apply to this tool. Write the reason in the notes. |

### 7.2 Rules for judging
1. Judge each answer against our use, not in general. A long retention period can be acceptable for public data and not acceptable for PHI.
2. A missing answer is "Follow-up", never "Acceptable".
3. For each deal-breaker, the answer must point to a contract, the BAA, the vendor's terms, or an independent report. A sales email or a marketing page is not enough.
4. If the vendor's answer and its contract disagree, the contract counts.
5. "We do not train on your data" does not mean "we do not keep your data". Read the answers to B1 and B4 together.
6. If the vendor uses another company's AI model or speech-to-text service, ask the same data questions about that company.
7. A BAA for the main product does not always cover a new AI feature. Check that the BAA names the feature, or covers all services.

## 8. The patient care questions (section K)

These questions apply only at Riverbend. Appendix A links each law.

| Question | Why we ask |
|---|---|
| K1. Recording consent | Our California clinics need the consent of all parties before they record a confidential conversation. Texas law asks us to tell patients when AI is used in their care. |
| K2. Audio and transcript retention | Visit audio is PHI. We want it kept for the shortest time that the note needs. |
| K3. Inputs to decision support tools | Section 1557 asks us to find out whether a decision support tool uses race, color, national origin, sex, age, or disability as an input. |
| K4. Messages to patients | In California, AI-generated clinical messages need a disclaimer and contact instructions, unless a licensed provider reviewed them. |

The Medical Director judges K3 and K4. The Privacy Officer judges K1 and K2.

## 9. Decide and record

The Summary sheet in the Excel file counts the statuses and shows one of these results:

| Result | What to do |
|---|---|
| Wait: answers missing or follow-up open | Finish the follow-up first. |
| Decide: some answers are not acceptable | The AI Review Group decides. Approve with conditions, approve a smaller use, or do not approve. |
| Do not approve as planned: a deal-breaker failed | Do not approve this use. Consider a smaller use, or another vendor. |
| Ready to decide: record the decision in the AI Tool Register | The AI Review Group decides and records the conditions. |

Then record the review in the AI Tool Register:

1. Set "Vendor terms: no training on our data?" from the answers to B1 and B2. For PHI, write "Yes" only if a signed BAA covers the AI feature.
2. Write the conditions that came from the review in "Conditions of use", for example "Consent script before each recording" or "Audio deleted after 30 days".
3. Use the risk score in the register to choose the approver.
4. Send the BAA and the contract terms that need changes to legal counsel.
5. File the Excel file and the evidence in the compliance folder on the shared drive.

## 10. Review the vendor again

| Tier | Review the vendor again at least every |
|---|---|
| Deep | 12 months |
| Standard | 24 months, or at contract renewal if sooner |
| Light | At contract renewal |

Review early if:

- the vendor changes the model or the speech-to-text service that a feature uses
- the vendor changes its data terms, its subcontractors, or its owner
- the vendor has a breach or a serious AI incident
- we start to use the tool with PHI, or for a new clinical use
- the tool gets new actions or new connections to our systems, for example write access to the EHR

## 11. Keep the evidence

For each review, keep:

- the completed Excel file
- the vendor's documents, for example the contract, the BAA, the security report, and the system card
- the follow-up emails
- the decision and the names of the AI Review Group members who decided

Keep them for the length of the contract plus 6 years.

## 12. Worked example: an ambient AI scribe

The Excel file in this folder shows a review in progress. The vendor is an example: "[Scribe vendor]". The scribe records visits with patient consent and drafts the visit note. The clinician reviews and signs each note.

- **Triage:** T1, T2, T5, and T6 are "Yes". The tier is Deep.
- **First round of answers:** the file holds the vendor's answers to the deal-breakers and the patient care questions.
- **What passed:** no training (B1), a BAA that names both subcontractors (H2), and a consent script (K1). Clinician sign-off (F3) and a tested switch-off (F4) also passed.
- **What needs follow-up:** retention is on a web page, not in the BAA (B4). Incident notice has no fixed number of days (G2). Clinicians cannot delete audio themselves (K2).
- **Result:** "Wait". The review owner sends one follow-up email and fills in the remaining answers.

---

## Appendix A. US laws behind this example

| Law | What it asks | Sections |
|---|---|---|
| HIPAA business associate rules ([45 CFR 164.502(e)](https://www.ecfr.gov/current/title-45/subtitle-A/subchapter-C/part-164/subpart-E/section-164.502#p-164.502%28e%29), [164.504(e)](https://www.ecfr.gov/current/title-45/subtitle-A/subchapter-C/part-164/subpart-E/section-164.504#p-164.504%28e%29)) | A BAA before a vendor creates, receives, keeps, or sends PHI. Return or destruction of PHI when the contract ends. | 6 (H2, B7), 7.2 |
| HIPAA Breach Notification Rule ([45 CFR 164.400–414](https://www.ecfr.gov/current/title-45/subtitle-A/subchapter-C/part-164/subpart-D)) | Notice to patients without unreasonable delay, and no later than 60 days after discovery | 6 (G2) |
| Section 1557 of the Affordable Care Act ([45 CFR 92.210](https://www.ecfr.gov/current/title-45/subtitle-A/subchapter-A/part-92/subpart-C/section-92.210)) | Reasonable efforts to find and reduce discrimination risk in patient care decision support tools | 8 (K3) |
| [California Health and Safety Code §1339.75](https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?lawCode=HSC&sectionNum=1339.75.) ([AB 3030](https://leginfo.legislature.ca.gov/faces/billNavClient.xhtml?bill_id=202320240AB3030)) | A disclaimer and contact instructions on AI-generated clinical messages, unless a licensed provider reviewed them | 8 (K4) |
| [California Penal Code §632](https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?lawCode=PEN&sectionNum=632.) | Consent of all parties before recording a confidential conversation | 6 (K1), 8 |
| [Texas HB 149](https://capitol.texas.gov/BillLookup/History.aspx?LegSess=89R&Bill=HB149), Texas Responsible AI Governance Act (from January 1, 2026) | Tell patients in plain language that AI is used in their care, by the date of service | 8 (K1) |

Status as of November 2026. Confirm with your counsel before you rely on any of these laws.

## Appendix B. Security risks

The questions cover risks from the [OWASP Top 10 for LLM Applications 2026](https://genai.owasp.org/resource/owasp-genai-llm-top-10-2026/).

The matching items are LLM01 Prompt Injection (C3), LLM02 Sensitive Information Disclosure (section B), and LLM03 Excessive Agency (section F).

They also include LLM04 Supply Chain (section D).

Laws and guidance change. This note is current as of November 2026.

---
*Fictional example by [NosisTech LLC](https://nosistech.com). Part of the [governance-templates](https://github.com/nosistech/governance-templates) collection. Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).*
