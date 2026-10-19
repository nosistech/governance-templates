# Using AI at Ardent Data: one-page guide (fictional example)

> This page is a summary. The full rules are in the Ardent Data AI Acceptable-Use Policy.

## Everyone

**Do**
1. Use approved tools only, with your Ardent account. The list is in the AI Tool Register.
2. Check the data tier before you paste or upload anything (table below).
3. Check every fact, number, and source in AI output.
4. Report fast in #security-incidents. We do not punish good-faith reports.

**Do not**
1. Do not use personal or free AI accounts for Ardent work.
2. Do not paste customer data into any chat or code assistant. Use the masked test data.
3. Do not put passwords, API keys, or other secrets into any AI tool.
4. Do not record a meeting without everyone's consent.
5. Do not send AI-drafted answers to a customer security questionnaire without a check by Security.

## Engineers

**Do**
1. Use code assistants on the business plan only.
2. Review and test AI-generated code like all other code. You own your pull request.
3. Give each agent its own credentials with the minimum access.
4. Run the evaluation and security test suite before you release an AI feature or change a model.

**Do not**
1. Do not give an AI agent write access to production.
2. Do not install an MCP server, plugin, or IDE extension that is not on the approved list.
3. Do not put secrets or another customer's data in a system prompt.
4. Do not change the model or model version without a change ticket.

## Data tiers

| Tier | Examples | Where it can go |
|---|---|---|
| 🟢 **Public** | Website, public docs, open-source code | Any approved tool |
| 🟡 **Internal** | Internal docs, roadmaps, our code without secrets | Approved business tools |
| 🔴 **Restricted** | All customer data, personal data, production data, unfixed vulnerabilities, secrets | Customer data: only the Ardent platform and listed model providers. Secrets: never |

**Not sure? Treat it as 🔴 Restricted.**

**Questions:** security@ardent.example or #security-help
