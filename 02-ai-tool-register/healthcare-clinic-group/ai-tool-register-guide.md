# AI Tool Register Guide: Riverbend Family Health (fictional example)

> **This is a fictional worked example.** Riverbend Family Health does not exist. Any resemblance to a real company is a coincidence. It shows how a US outpatient clinic group could adapt the [generic template](../generic/ai-tool-register-guide.md). Laws change and differ by state. Ask your legal counsel and your HIPAA Privacy Officer to review your own register. This example is not legal advice.
>
> Open to use and adapt under the license.

| Document control | |
|---|---|
| Company | Riverbend Family Health (6 family-medicine clinics: 4 in Texas, 2 in California, about 120 staff) |
| Register owner | Chief Operating Officer |
| Approved by | Chief Executive Officer and Medical Director |
| Effective date | November 1, 2026 |
| Version | 1.0 |
| Next review of this guide | October 31, 2027 |

---

## 1. Purpose

The Riverbend AI Tool Register is the list of every AI tool that our clinics use, with a risk score for each use. It answers 4 questions:

1. Which AI tools do we use, and for what?
2. Who is responsible for each one?
3. How risky is each use for our patients and their health information?
4. Is each use approved, approved with conditions, or not allowed?

Our AI Acceptable-Use Policy tells the workforce to use only approved tools. This register is where we write down "approved". When a patient, an auditor, a payer, or a regulator asks "which AI do you use?", this register is the answer.

## 2. What goes in the register

### 2.1 One row for each use, not for each vendor
The same tool can be safe for one task and risky for another. An AI assistant that drafts staff schedules is low risk. The same assistant that drafts replies to patients about test results is high risk. Give each use its own row.

### 2.2 Include all of these
- the ambient AI scribe in our electronic health record (EHR)
- the AI assistant that drafts replies to patient portal messages
- the AI scheduling assistant on our website and phone line
- the AI features in our office software, email, and practice-management system
- clinical decision support tools that give risk scores or alerts, including the scores inside the EHR
- AI tools for medical coding and billing
- meeting notetakers, browser extensions, and AI agents
- personal AI accounts, with the status "Prohibited", so that the decision is on record

### 2.3 What we do not register
We do not register spell check and grammar suggestions that do not send data outside the software. If a feature can see PHI, we register it. If you are not sure, register it.

### 2.4 Two terms
- **PHI (protected health information):** any information that identifies a patient and relates to their health, their care, or their payment for care.
- **BAA (Business Associate Agreement):** the contract that HIPAA requires before a vendor can create, receive, keep, or send PHI for us.

## 3. Roles

| Role | Who | Responsibilities |
|---|---|---|
| Register owner | Chief Operating Officer | Keeps the register complete and current. Runs the reviews. Reports to the CEO. |
| AI Review Group | Chief Operating Officer, Privacy Officer, Security Officer, Medical Director | Decides on High and Critical uses, and on every use that touches PHI or patient care |
| HIPAA Privacy Officer | Compliance Manager | Confirms that a signed BAA covers the AI feature before any PHI goes to it |
| HIPAA Security Officer | IT Manager | Sets up each tool, controls access, keeps logs, and switches tools off when needed |
| Medical Director | Lead physician | Owns the clinical safety of each AI tool. Leads the yearly bias review of decision support tools. |
| Tool owner | One named person for each row | Knows how the tool is used. Keeps the row correct. Can switch the tool off. |
| Workforce | Everyone | Ask before you use a new tool or a new use. Report AI tools that are not in the register. |

## 4. How a new use gets into the register

1. A workforce member fills in the AI Tool Request Form and sends it to the AI Review Group.
2. The register owner adds a row with the status "Under review".
3. The Privacy Officer checks whether the use touches PHI. If it does, the Privacy Officer checks the BAA.
4. The register owner and the tool owner score the risk (section 6).
5. The approver for that risk level decides (section 7).
6. The register owner records the decision, the conditions, the approver, and the date.
7. The register owner tells the person who asked. We decide within 5 business days. Clinical uses can take longer, because the Medical Director must review them.

## 5. The columns

The columns are the same as in the generic template. At Riverbend, we fill in 4 of them in a special way:

| Column | What to write at Riverbend | Example |
|---|---|---|
| Highest data tier | Any PHI makes the tier Restricted. | Restricted |
| Affects decisions about people? | Yes for every use that supports a decision about a patient's care, or about a staff member's job | Yes |
| Vendor terms: no training on our data? | For PHI, write "Yes" only if a signed BAA covers the AI feature. A BAA for the main product does not always cover a new AI feature. | Yes |
| Conditions of use | Write who must review the output: a clinician, a coder, or a manager | A clinician reads and corrects every note before signing |

## 6. How to score the risk

### 6.1 Ask "what could go wrong?"
For each use, write down the worst thing that could credibly happen to a patient or to their data. Use these risks as a checklist:

- **PHI leaks:** the tool exposes patient information, or sends it to a vendor without a BAA.
- **Wrong clinical content:** the tool invents a symptom, a dose, an allergy, or a diagnosis, and someone relies on it.
- **Unfair results:** a risk score works less well for one group of patients.
- **Hidden instructions:** a website, an email, or a document tells the AI tool to do something harmful. Experts call this "prompt injection".
- **Too much power:** an agent sends, deletes, or changes something that nobody approved.
- **Vendor problems:** the vendor changes its terms, its model, or its owner, or it has a breach.

### 6.2 Likelihood and impact
We use the same 1 to 5 scales as the generic template. The "Scoring guide" sheet in the Excel file has them.

**Risk score = likelihood × impact.** The score goes from 1 to 25.

| Score | Risk level |
|---|---|
| 1–4 | Low |
| 5–9 | Medium |
| 10–15 | High |
| 16–25 | Critical |

### 6.3 Scoring rules at Riverbend
1. Score the use as it runs today, with the controls that are really in place. A control that is only planned does not count yet.
2. If you are not sure between two numbers, choose the higher one.
3. If the use supports a clinical decision or sends clinical content to patients, the impact is at least 4.
4. If the use affects decisions about staff, the impact is at least 4.
5. If the use touches PHI and no signed BAA covers it, the status is "Prohibited". We do not score it until a BAA exists.
6. Two people score each High or Critical use: the tool owner and the register owner. The Medical Director joins for every clinical use.

## 7. Decisions

### 7.1 Who decides

| Risk level | Who approves | What the approver does |
|---|---|---|
| Low | The tool owner's manager | Approves with the standard rules in our AI Acceptable-Use Policy |
| Medium | Chief Operating Officer and IT Manager | Approves with written conditions of use |
| High | AI Review Group | Approves only with conditions and a written plan to lower the score |
| Critical | Nobody, until the score goes down | Change the use or add controls until the score is 15 or lower. Only the CEO and the Medical Director together can accept a Critical risk, in writing, for a limited time. |

**Any use that touches PHI or patient care goes to the AI Review Group**, whatever its risk level. The Medical Director must agree to every clinical use.

### 7.2 Status

| Status | Meaning |
|---|---|
| Approved | The workforce can use the tool for this use, under our AI Acceptable-Use Policy. |
| Approved with conditions | The workforce can use it, but only under the conditions in the row. |
| Under review | Do not use it yet. We are deciding. |
| Prohibited | Do not use it for Riverbend work. |
| Retired | We stopped using it. The row stays for our records. |

### 7.3 Uses that affect patients
A clinician makes every clinical decision. AI tools support clinicians. They do not diagnose patients or decide treatment. Write this in the conditions of use for every clinical row.

Every year, the Medical Director reviews each decision support tool for the risk of discrimination against patient groups. Section 1557 of the Affordable Care Act requires reasonable efforts to find and reduce this risk.

## 8. Keep the register current

### 8.1 Review schedule

| Risk level | Review at least every |
|---|---|
| Critical and High | 3 months |
| Medium | 6 months |
| Low | 12 months |

The Excel file calculates the next review date. Decision support tools also get the yearly bias review in section 7.3.

### 8.2 Review early if
- the vendor changes its model, its terms, or its owner
- the vendor changes or ends its BAA
- the tool starts to see PHI, or more PHI than before
- patients start to see the output or talk to the tool
- an agent gets new permissions
- an incident or a near miss happens
- a new law applies to the use, for example a new state rule on AI in health care

### 8.3 Find the tools that are not in the register
Every 3 months, each clinic manager asks their team which AI tools they use. The IT Manager also checks the AI features that our EHR and office software added since the last check. Add each new use with the status "Under review".

### 8.4 Retire a tool
1. Remove the accounts and the connections. Revoke the API keys.
2. Export the records that we must keep, for example signed clinical notes.
3. Ask the vendor to return or destroy all PHI, as the BAA requires. Keep the written confirmation.
4. Change the status to "Retired" and write the date.

### 8.5 Change log
Record every change to the register in the "Change log" sheet: the date, the ID, the change, and who made it.

---

## Appendix A. Health-care laws behind this example

Status as of November 2026. Confirm with your counsel before you rely on any of them.

| Rule | What it requires | Sections in this guide |
|---|---|---|
| HIPAA Privacy Rule, minimum necessary standard ([45 CFR 164.502(b)](https://www.ecfr.gov/current/title-45/subtitle-A/subchapter-C/part-164/subpart-E/section-164.502#p-164.502%28b%29)) | Use and share only the minimum PHI that a task needs | 5, 6 |
| HIPAA business associate rules ([45 CFR 164.502(e)](https://www.ecfr.gov/current/title-45/subtitle-A/subchapter-C/part-164/subpart-E/section-164.502#p-164.502%28e%29), [164.504(e)](https://www.ecfr.gov/current/title-45/subtitle-A/subchapter-C/part-164/subpart-E/section-164.504#p-164.504%28e%29)) | A BAA before a vendor creates, receives, keeps, or sends PHI. Return or destruction of PHI when the contract ends. | 4, 5, 6.3, 8.4 |
| HIPAA Breach Notification Rule ([45 CFR 164.400–414](https://www.ecfr.gov/current/title-45/subtitle-A/subchapter-C/part-164/subpart-D)) | Notice to patients without unreasonable delay, and no later than 60 days after discovery | 8.2 |
| Section 1557 of the Affordable Care Act ([45 CFR 92.210](https://www.ecfr.gov/current/title-45/subtitle-A/subchapter-A/part-92/subpart-C/section-92.210)) | Reasonable efforts to find and reduce discrimination risk in patient care decision support tools | 7.3, 8.1 |
| [California Health and Safety Code §1339.75](https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?lawCode=HSC&sectionNum=1339.75.) ([AB 3030](https://leginfo.legislature.ca.gov/faces/billNavClient.xhtml?bill_id=202320240AB3030)) | A disclaimer and contact instructions on AI-generated clinical messages, unless a licensed provider reviewed them | 5, Register |
| [California Penal Code §632](https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?lawCode=PEN&sectionNum=632.) | Consent of all parties before recording a confidential conversation | Register (AI scribe) |
| [Texas HB 149](https://capitol.texas.gov/BillLookup/History.aspx?LegSess=89R&Bill=HB149), Texas Responsible AI Governance Act (from January 1, 2026) | Tell patients in plain language that AI is used in their care, by the date of service | Register |
| [Texas SB 1188](https://capitol.texas.gov/BillLookup/History.aspx?LegSess=89R&Bill=SB1188) (Health and Safety Code §183.005, from September 1, 2025) | A practitioner who uses AI for diagnosis reviews all AI-generated records and tells the patient | 7.3, Register |

## Appendix B. Security risks

The risks in section 6.1 match the [OWASP Top 10 for LLM Applications 2026](https://genai.owasp.org/resource/owasp-genai-llm-top-10-2026/).

The matching items are LLM01 Prompt Injection, LLM02 Sensitive Information Disclosure, and LLM03 Excessive Agency.

They also include LLM04 Supply Chain and LLM07 Misinformation.

Laws and guidance change. This note is current as of November 2026.

---
*Fictional example by [NosisTech LLC](https://nosistech.com). Part of the [governance-templates](https://github.com/nosistech/governance-templates) collection. Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).*
