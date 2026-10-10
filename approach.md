# Approach — Home Credit LAP Qualification Voice Agent

## 1. Objective

The objective of this project is to build a voice-based AI agent that qualifies customers interested in a Home Credit Loan Against Property (LAP).

The agent collects relevant information, checks eligibility against the configured requirements, handles customer questions and corrections, and provides an appropriate closing.

## 2. Agent Design

The voice agent is named **Priya** and is configured to communicate in English using a female voice.

The agent uses the customer's name through the dynamic variable `{{customer_name}}`, allowing the name to be supplied at call time rather than hardcoded into the prompt.

The agent is designed to keep conversations clear, polite, and focused on the qualification process.

## 3. Conversation Flow

The intended conversation follows these stages:

1. **Greeting and identity verification:** Introduce the agent and verify the customer's identity.
2. **Availability and consent:** Confirm that the customer can continue and agrees to answer the qualification questions.
3. **Eligibility information collection:** Ask the required questions about the customer's property, documents, income, loan amount, ownership, existing loan situation, and tenure.
4. **Eligibility evaluation:** Compare the customer's responses with the configured eligibility rules.
5. **Routing or disqualification:** Explain when a condition is not met and follow the configured handling for existing-loan or EMI-reduction enquiries.
6. **Closing:** Provide an appropriate closing without claiming that a lead, callback, or specialist notification has been created unless that functionality actually exists.

## 4. Prompt Engineering Strategy

The system prompt defines the agent's role, communication style, qualification process, and boundaries.

The prompt is designed to:

- Ask clear questions and collect the required information.
- Handle answers given in a different order.
- Ask for clarification when a response is ambiguous.
- Accept customer corrections and use the corrected answer.
- Follow disqualification conditions consistently.
- Avoid inventing approvals, callbacks, notifications, or completed actions.
- Handle interruptions and situations where no response is needed.

The configured loan amount limit is up to ₹75 lakh, subject to the eligibility conditions in the prompt.

## 5. Testing Strategy

Testing uses Retell AI web-call sessions to examine how the agent behaves in different situations.

The planned test scenarios include:

- A customer who meets the eligibility requirements.
- An ineligible property type.
- Required documents that are unavailable.
- Income that does not meet the configured requirement.
- A customer requesting more than the maximum amount.
- Joint property ownership.
- Existing loan or EMI-reduction enquiries.
- Customer unavailability or a callback request.
- A tenure that falls outside the permitted range.
- Answers supplied out of order.
- Ambiguous document availability.
- A customer correcting a previously supplied answer.

The test cases should be mapped to actual session transcripts before a scenario is marked as passed or failed.

## 6. Evaluation Metrics

The following metrics are used to review the initial calls:

- Session outcome reported by Retell AI.
- Call duration.
- End-to-end latency.
- User sentiment.
- Call cost.
- Correctness of the agent's responses and eligibility decisions, verified from transcripts.

Platform session outcomes are useful indicators but do not replace manual review of functional correctness.

## 7. Current Status

Initial Retell AI call sessions have been recorded. The testing report contains the call summary, including successful and unsuccessful session counts, total cost, duration, and latency.

The next stage is to review the unsuccessful calls, verify the qualification logic, and complete scenario-level testing.

## 8. Expected Outcome

The intended outcome is a reliable voice agent that conducts a structured LAP qualification conversation, follows the configured eligibility rules, handles unexpected responses appropriately, and communicates clearly without making unsupported promises.
