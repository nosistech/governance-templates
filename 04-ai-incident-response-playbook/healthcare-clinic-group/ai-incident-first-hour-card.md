# AI Incident: First-Hour Card (Riverbend Family Health, fictional example)

> **This is a fictional worked example.** Riverbend Family Health does not exist. Any resemblance to a real company is a coincidence. The full steps are in the Riverbend AI Incident Response Playbook. This example is not legal advice.
>
> Open to use and adapt under the license.

## If you see a problem with an AI tool

1. **Stop.** Do not send, publish, or act on the output.
2. **Keep everything.** Do not delete the chat, the output, or the file.
3. **Take a screenshot** that shows the date and time.
4. **Report it at once** to the incident lead: the Compliance Manager, extension 2200 (after hours: the IT on-call line).
5. **Write down** what you saw, which tool, when, and who else saw it.

If the problem can harm a patient, also tell the patient's doctor at once.

Do not ask the AI to explain what went wrong. Its answer is a guess, not a record. If you are not sure that it is a problem, report it anyway. We do not blame people for reports.

## First hour: for the incident lead

| # | Step | Done |
|---|---|---|
| 1 | Open a row in the incident log. Write the date and time of discovery. | ☐ |
| 2 | Confirm who leads. | ☐ |
| 3 | Rate the severity in 5 areas: people, data, money, operations, trust and legal. The highest level wins. | ☐ |
| 4 | If harm to people continues, switch off the tool now. Write down what and when. | ☐ |
| 5 | Save the evidence: prompts, outputs, settings, model version, agent actions, logs. | ☐ |
| 6 | Contain: choose the smallest action that stops the harm. | ☐ |
| 7 | Find the reach: which users, customers, records, and decisions, and since when. | ☐ |
| 8 | Call the vendor. Ask what changed, and ask them to keep their logs. | ☐ |
| 9 | Tell the privacy and legal contact if the incident touches personal data, a customer, or a contract. | ☐ |
| 10 | Ask the executive to confirm the severity and the next update time. | ☐ |

## Severity at a glance

| Severity | Typical sign | Start within | Executive hears |
|---|---|---|---|
| SEV1 | A patient is harmed, PHI is outside Riverbend, or money moved without approval | 1 hour | At once |
| SEV2 | A wrong output reached a patient or a signed note, with no confirmed harm yet | 4 hours | The same day |
| SEV3 | The problem stayed inside the company | 1 day | Monthly report |
| SEV4 | Near miss: caught before it harmed anyone | 5 days | Monthly report |

## Contacts

| Role | Name | Phone | Backup |
|---|---|---|---|
| Incident lead | Compliance Manager | Extension 2200 | IT Manager, extension 2210 |
| Executive with switch-off authority | Chief Executive Officer | Extension 2100 | Medical Director, extension 2120 |
| IT or technical responder | IT Manager | Extension 2210 | IT on-call line |
| Privacy and legal contact | Compliance Manager, with outside healthcare counsel | Extension 2200 | Counsel's number in the Compliance folder |
| Communications | Practice Administrator | Extension 2150 | Chief Executive Officer |
| Insurer: claims line | Cyber insurer (policy number in the Compliance folder) | Claims line in the Compliance folder |  |
| Main AI vendors: support | EHR vendor (AI scribe, portal replies) | Priority support line |  |

---
*Fictional example by [NosisTech LLC](https://nosistech.com). Part of the [governance-templates](https://github.com/nosistech/governance-templates) collection. Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).*
