# SalesAgents AI – Home Credit Loan Against Property Voice Agent

## 1. Project Overview

This project is part of the SalesAgents AI – AI Intern Prompt Engineer assignment from NxtWave.

The goal is to configure an AI-powered voice agent that communicates with existing Home Credit customers and checks their initial eligibility for a Loan Against Property (LAP).

The voice agent is named **Ananya – Home Credit LAP**. It is designed to conduct a natural conversation, verify the customer's identity, collect eligibility information, and explain the next steps.

The agent is configured using **Retell AI**.

## 2. Project Objectives

- Create an AI voice agent for Loan Against Property qualification.
- Verify the customer's identity before discussing the offer.
- Explain the available loan offer clearly.
- Collect and remember customer information during the conversation.
- Identify eligible and ineligible customers based on the specified rules.
- Handle customer questions, interruptions, and out-of-order answers.
- End the conversation politely when the customer declines or fails a mandatory eligibility requirement.
- Direct eligible customers to the next stage of the loan process.

## 3. Technology Used

- **Retell AI:** Voice agent configuration and conversation management.
- **AI Language Model:** Understands customer responses and generates conversational replies.
- **Speech Recognition and Voice Generation:** Supports spoken customer-agent interactions.
- **Prompt Engineering:** Defines the agent's role, conversation flow, eligibility conditions, and response rules.

## 4. Agent Configuration

| Setting | Details |
|---|---|
| Agent name | Ananya – Home Credit LAP |
| Platform | Retell AI |
| Language | English (US) |
| Voice | Lily |
| Conversation type | AI-powered voice conversation |
| Opening message | Greets the customer and verifies their identity |
| Customer placeholder | `{{customer_name}}` |
| Default sample customer | Rahul Sharma |

## 5. Loan Offer

The agent explains that eligible existing customers may be considered for a Loan Against Property of up to **₹75,00,000 (₹75 lakh)**.

The agent does not guarantee loan approval or invent an interest rate. Final approval, applicable interest rates, and further loan details are to be confirmed by the appropriate Home Credit representative.

## 6. Conversation Flow

### Step 1: Customer Verification

The agent greets the customer and confirms whether it is speaking to the intended person.

The loan offer is discussed only after the customer's identity is confirmed.

### Step 2: Customer Availability

If the customer is busy, the agent asks about their preferred callback time and ends the current conversation politely.

The agent does not claim that a callback has been scheduled unless an actual scheduling mechanism confirms it.

### Step 3: Explain the Offer

After verification, the agent explains the Loan Against Property offer and its maximum amount.

### Step 4: Collect Eligibility Information

The agent collects the following seven details:

1. **Property type:** Residential, Commercial, Industrial, or Agricultural.
2. **Property ownership:** Sole ownership or joint ownership.
3. **Original property documents:** Whether the original documents are available.
4. **Loan amount required:** The amount requested by the customer.
5. **Income source:** Salaried or self-employed, with income received through a bank account.
6. **Property market value:** The estimated current market value of the property.
7. **Repayment tenure:** The requested repayment period in years.

The agent should remember information already provided and avoid asking the same question again. If the customer provides answers out of order, the agent should retain those answers and collect only the missing details.

### Step 5: Check Eligibility

The agent evaluates the collected information against the assignment's eligibility rules.

Customers who fail a mandatory condition are informed politely that they do not meet the specified criteria, and the conversation is ended appropriately.

### Step 6: Handle Special Cases

The agent handles requests above ₹75 lakh, existing loan-transfer enquiries, busy customers, and customers who decline the offer according to the defined conversation rules.

### Step 7: Next Steps

If the customer satisfies all specified initial eligibility conditions, the agent explains that a senior expert will contact them regarding the next steps and the applicable interest rate.

The agent does not represent initial eligibility as final loan approval.

## 7. Eligibility Rules

| Condition | Agent behaviour |
|---|---|
| Residential property | Continue eligibility checks |
| Commercial property | Continue eligibility checks |
| Industrial property | Continue eligibility checks |
| Agricultural property | Disqualify according to the assignment rules |
| Sole property ownership | Accept |
| Joint property ownership | Accept |
| Original property documents unavailable | Disqualify according to the assignment rules |
| Loan amount within the ₹75 lakh limit | Continue eligibility checks |
| Loan amount above ₹75 lakh | Explain the maximum offer and ask whether the customer wishes to consider an alternative within the limit |
| Salaried income received through a bank | Accept for further checks |
| Self-employed income received through a bank | Accept for further checks |
| Income received only in cash | Disqualify according to the assignment rules |
| Repayment tenure from 3 to 15 years, inclusive | Continue eligibility checks |
| Repayment tenure below 3 years or above 15 years | Disqualify according to the assignment rules |
| Existing loan or request to reduce an EMI | Direct to a loan-transfer specialist and end the current qualification flow |
| Customer declines | Respect the decision and stop the conversation |
| Incorrect customer identity | Do not disclose the offer; end the conversation appropriately |

**Note:** Passing these initial checks does not guarantee loan approval.

## 8. Conversation Design Principles

The prompt is designed to encourage the agent to:

- Speak politely and naturally.
- Ask one question at a time.
- Avoid unnecessary repetition.
- Remember information already shared.
- Handle interruptions and out-of-order answers.
- Avoid pressuring customers who decline.
- Avoid unsupported financial claims.
- Follow mandatory disqualification rules.
- End conversations appropriately when required.

## 9. Prepared Simulation Test Cases

Eleven simulation test cases have been prepared in Retell AI to cover different conversation scenarios.

| No. | Test case | Purpose |
|---|---|---|
| 1 | Eligible Residential Property Customer | Check the normal eligibility flow |
| 2 | Agricultural Property — Disqualification | Check property-based disqualification |
| 3 | Missing Original Property Documents | Check document availability rules |
| 4 | Cash Income — Disqualification | Check income eligibility |
| 5 | Loan Amount Above ₹75 Lakh | Check handling of requests exceeding the maximum offer |
| 6 | Repayment Tenure Outside Range | Check the minimum and maximum tenure rules |
| 7 | Existing Loan — EMI Reduction | Check specialist referral behaviour |
| 8 | Busy Customer — Callback Request | Check callback preference handling |
| 9 | Out-of-Order Answers — Memory Check | Check information retention |
| 10 | Wrong Customer Identity | Check identity verification |
| 11 | Customer Declines — Stop Call | Check respectful conversation termination |

**Testing status:** The eleven test cases have been prepared and saved. Simulation execution and test results have not yet been completed.

## 10. Limitations and Scope

- The agent performs initial qualification based on the configured prompt.
- It does not independently verify financial documents or property ownership.
- It does not approve or sanction loans.
- It does not calculate or guarantee a final interest rate.
- Callback scheduling and specialist transfers depend on the availability of connected systems or actual business processes.
- The configured eligibility rules are for the assignment demonstration and should not be treated as an official loan approval policy.

## 11. Project Link

**Platform:** Retell AI

**Published interactive agent:**  
[Open Ananya – Home Credit LAP](https://agent.retellai.com/orb/agent_8cfc8bd9e00d45f2f35661e8a5?token=57e575996a42d6fcf345cc3ee2570f13)

The link opens the interactive voice agent. It is not a test report or call recording.

## 12. Conclusion

This project demonstrates how prompt engineering can be used to configure a conversational AI voice agent for initial Loan Against Property qualification.

The solution focuses on customer identity verification, structured information collection, eligibility rule handling, memory of customer responses, special-case handling, and clear communication of next steps.

The prepared simulation scenarios provide a basis for future validation of the agent's behaviour.
