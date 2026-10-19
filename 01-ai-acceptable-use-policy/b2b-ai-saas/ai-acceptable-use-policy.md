# AI Acceptable-Use Policy: Ardent Data, Inc. (fictional example)

> **This is a fictional worked example.** Ardent Data, Inc. does not exist. It shows how a B2B software company that builds an AI product could adapt the [generic template](../generic/ai-acceptable-use-policy.md). Ask your legal counsel to review your own policy. This example is not legal advice.
>
> Free to use and adapt.

| Document control | |
|---|---|
| Company | Ardent Data, Inc.: a multi-tenant AI platform that lets mid-size companies search, summarize, and automate work on their own documents. About 45 staff, remote-first, customers in the US and the EU. |
| Policy owner | Head of Security and Compliance |
| Approved by | Chief Executive Officer and Chief Technology Officer |
| Effective date | November 1, 2026 |
| Version | 1.0 |
| Next review | October 31, 2027 |

---

## 1. Purpose

Ardent Data uses AI in two ways. Our staff use AI tools to do their work, and our product uses AI to serve our customers. This policy sets the rules for both. It protects our customers' data, keeps the promises in our customer contracts, and keeps our product secure.

## 2. Scope

### 2.1 Who this policy applies to
This policy applies to all employees, contractors, and interns, in all countries. Vendors that process our data or our customers' data must follow the AI terms in their contracts.

### 2.2 What this policy applies to
- **AI tools that staff use:** chat assistants, code assistants, AI agents, notetakers, browser extensions, and AI features inside our business software.
- **AI in our product:** the large language models (LLMs) and other AI components in the Ardent platform. This includes the customer data that they process.

The Ardent Secure Development Standard gives the detailed engineering steps for the product. This policy sets the rules that the standard must follow.

### 2.3 Definitions
- **Customer data:** all data that a customer or its users put into the Ardent platform, including documents, prompts, outputs, embeddings, logs, and files.
- **Model provider:** a company whose AI model our product calls through an API.
- **Sub-processor list:** the public list of vendors that process customer data for us. Our customer contracts require us to keep it current.
- **MCP server:** a connector that gives an AI tool access to other software or data. MCP stands for Model Context Protocol.
- **Approved tool:** an AI tool with the status "Approved" or "Approved with conditions" in the Ardent AI Tool Register.

## 3. Roles

| Role | Who | Responsibilities |
|---|---|---|
| Policy owner | Head of Security and Compliance | Keeps this policy current, approves exceptions, answers customer security questions |
| AI Review Group | Head of Security and Compliance, CTO, Head of Product, privacy counsel | Approves new AI tools, new model providers, and new AI features in the product |
| Tool owner | One named person for each approved tool and each AI feature | Sets up the tool or feature, controls access, monitors it, can switch it off |
| Engineering leads | All team leads | Make sure that their teams follow sections 6 and 7 |
| All staff | Everyone in scope | Follow this policy and report problems |

## 4. Approved tools and new requests

1. Use only approved tools for Ardent work, with your Ardent account. The list is in the AI Tool Register.
2. Never use a personal account or a free AI tool for Ardent work.
3. To request a new tool, open a ticket in the security queue. Give the tool name, the task, and the data that the tool will see. We decide within 5 business days.
4. MCP servers, plugins, and IDE extensions count as tools. Install only the ones on the approved list.
5. A new model provider for the product needs approval from the AI Review Group. Before it processes customer data, we update the sub-processor list and give customers the notice that their contracts require.

## 5. Data rules

| Tier | Examples | Tools you can use |
|---|---|---|
| **Public** | Our website, public documentation, open-source code, published blog posts | Any approved tool |
| **Internal** | Internal documents, roadmaps, and our own source code without secrets | Approved business tools that do not let the vendor train its AI on our data |
| **Restricted** | All customer data. Also personal data, production database content, details of unfixed security vulnerabilities, unreleased financial results, passwords, API keys, and other secrets. | **Customer data:** only inside the Ardent platform and the model providers on our sub-processor list. **Secrets:** never, in any AI tool. |

Also follow these rules:

- If you do not know the tier, treat the data as Restricted.
- Do not paste customer data into a chat assistant or a code assistant to debug a problem. Use the masked test data set, or ask Security for an approved tool.
- If a customer gives you written permission to use its data for a specific task, store the permission in the customer record first.

## 6. Engineering with AI

1. Use code assistants on the business plan only. The register shows the approved plan for each tool.
2. Never put secrets into a prompt. Our repositories run secret scanning on every commit.
3. Review and test all AI-generated code like all other code. The author of the pull request is responsible for it.
4. Check the license of any code that an AI tool suggests from outside sources. Do not add code that has an unknown or incompatible license.
5. AI coding agents work in development environments only. They must not have write access to production.
6. A person must approve each agent action that is difficult to reverse. Examples: a database migration, a deployment, a deletion, or a change to access rights.
7. Give each agent its own credentials with the minimum access that it needs. Do not let an agent use your personal credentials.

## 7. AI in our product

These rules keep the promises that we make to customers. The Secure Development Standard explains how we meet them.

1. **No training on customer data.** We do not use customer data to train or fine-tune any AI model, unless a customer agrees in writing.
2. **Model provider terms.** Each model provider must contractually agree not to train on customer data. Each provider must also meet our retention limits.
3. **Tenant isolation.** One customer's data must never appear in another customer's results. This includes search results, embeddings, caches, and agent memory.
4. **Testing before release.** Before we release an AI feature or change a model, we run our evaluation and security test suite. The suite covers prompt injection, data leakage, and unsafe agent actions.
5. **Model changes.** A change of model or model version is a product change. It goes through change management, and we tell customers about major changes.
6. **Logging.** We log AI requests, responses, and agent actions for each tenant. We keep the logs for the period in our customer contracts.
7. **Switch off.** Each AI feature has a switch that can turn it off for one customer or for all customers.
8. **Transparency.** Our product tells users when they interact with AI. Our documentation explains what each AI feature does and its known limits.
9. **Usage limits.** Each tenant and each AI feature has rate limits and spending alerts.
10. **Hidden instructions.** System prompts and other hidden context must not contain secrets or another customer's data. Assume that a user can make the AI reveal them.

## 8. Allowed and prohibited uses

### 8.1 Allowed uses
With approved tools and data of the correct tier, you can use AI to:

- write, review, test, and document code
- draft documents, emails, and support replies for you to review
- summarize meetings, documents, and research
- analyze product data, if the AI Tool Register approves the tool for that data tier

### 8.2 Prohibited uses
Do not use any AI tool to:

- give customer data to a tool that is not approved for customer data
- make a final decision about an employee or a job applicant
- copy the voice, face, or writing of a real person without their permission
- record a meeting without the consent of all participants. Many customer and EU meetings need explicit consent.
- test attacks against systems that we do not own, or against customer environments without written permission
- create false or misleading content, including marketing claims about our AI that we cannot prove

## 9. Check the output

1. You are responsible for all work that you deliver, including work that AI helped to make.
2. Check all facts, numbers, and sources in AI output before you use it.
3. Security must check every AI-drafted answer to a customer security questionnaire before we send it. A wrong answer in a questionnaire can become a contract commitment.
4. Marketing and sales claims about our AI features need approval from the Head of Product.

## 10. Training

1. Complete the AI training within 30 days after you join, and a refresher every 12 months.
2. Engineers also complete the secure AI engineering module. It covers the OWASP Top 10 for LLM Applications and our agent rules.
3. The training also meets the AI literacy duty of the EU AI Act for staff who work with our EU customers.

## 11. Report problems

Report immediately in the #security-incidents channel, or to security@ardent.example, if:

- customer data went into a tool that is not approved for it
- one customer's data appeared in another customer's results
- an AI feature or agent did something unexpected or unsafe
- you found a prompt injection or another AI vulnerability in our product
- a model provider changed its model or terms without notice

Report even if you are not sure. We do not punish good-faith reports of mistakes. The AI incident-response playbook explains what happens next.

## 12. Exceptions, enforcement, and review

1. **Exceptions:** Ask the policy owner in a ticket. Give the reason, the time limit, and the extra controls. Exceptions for customer data also need the CTO.
2. **Enforcement:** If you do not follow this policy, you can lose access to AI tools and systems. Disciplinary action is also possible, as our other policies and the law allow.
3. **Your rights:** This policy does not limit your rights under the law, including your right to discuss the terms and conditions of your employment.
4. **Monitoring:** Ardent keeps logs of staff AI tool use for 90 days to protect customer data, as the law allows.
5. **Review:** The policy owner reviews this policy at least every 12 months. The policy owner also reviews it after a serious AI incident, when a law changes, or when a model provider changes its terms.

---

## Acknowledgement

I read the Ardent Data AI Acceptable-Use Policy. I understand it, and I agree to follow it.

| Name | Team | Signature | Date |
|---|---|---|---|
| | | | |

---

## Appendix A. Answers for customer security reviews

Enterprise customers ask the same AI questions in most security reviews. This table shows where this policy answers them. Attach the evidence when you reply.

| Common customer question | Answer in this policy | Evidence to attach |
|---|---|---|
| Do you train AI models on our data? | 7.1, 7.2 | Customer contract clause, model provider terms |
| Which AI vendors process our data? | 4.5, 7.2 | Sub-processor list |
| How do you keep our data separate from other customers? | 7.3 | Architecture diagram, test results |
| How do you test for prompt injection and data leakage? | 7.4 | Summary of the latest security test |
| Will you tell us before you change the AI model? | 7.5 | Change-notice clause, change log |
| Can you switch off an AI feature for our account? | 7.7 | Feature-control screenshot |
| How do you control AI coding tools and agents? | 6 | AI Tool Register extract |
| Do your staff get AI training? | 10 | Training completion report |
| What happens if an AI incident affects our data? | 11 | AI incident-response playbook |

## Appendix B. Framework mapping

The generic template has the full section-by-section mapping. This example adds product controls that support these items:

- **OWASP Top 10 for LLM Applications 2026:**
  - LLM01 Prompt Injection: 7.4
  - LLM02 Sensitive Information Disclosure: 5, 7.3
  - LLM03 Excessive Agency: 6.5–6.7
  - LLM04 Supply Chain: 4.4–4.5
  - LLM06 Unbounded Consumption: 7.9
  - LLM08 Hidden Context Exposure: 7.10
  - LLM09 Vector and Embedding Weaknesses: 7.3
- **NIST AI 600-1:** GV-6.1-007 (approved provider list), GV-1.6-002 (AI inside other software), MG-2.4-004 (criteria to switch off a system)
- **NIST AI RMF 1.0:** GOVERN 6.1 (third-party risks), MANAGE 2.4 (switch off), MANAGE 4.3 (incident communication)
- **ISO/IEC 42001, Annex A areas:** A.6 (AI system life cycle), A.7 (data for AI systems), A.10 (third-party and customer relationships)
- **EU AI Act:** Article 4 (AI literacy) and Article 50 (transparency when people interact with AI). Ask counsel to confirm your role (provider or deployer) for each AI feature.

---
*Fictional example by [NosisTech LLC](https://nosistech.com). Part of the free [governance-templates](https://github.com/nosistech/governance-templates) collection. Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).*
