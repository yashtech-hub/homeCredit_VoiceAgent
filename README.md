# Home Credit Voice Agent

## Project Overview

This project focuses on designing and testing an AI voice agent for initial qualification calls for a Home Credit Loan Against Property (LAP) offer of up to ₹75,00,000, subject to eligibility and further assessment.

The voice agent is named Priya. She communicates in clear, professional English and guides customers through the initial qualification process.

The agent is a qualification assistant, not a loan approval officer. Passing the initial qualification does not guarantee loan approval, an interest rate, or disbursement.

## Objectives

- Design a structured system prompt for an AI voice agent.
- Verify customer identity and check availability before starting qualification.
- Collect and validate the required eligibility information.
- Handle disqualification scenarios correctly.
- Handle customer corrections, ambiguous answers, and answers given out of order.
- Route existing property loan and EMI-reduction enquiries away from the standard qualification flow.
- Test the agent using different customer scenarios.
- Document test results and prompt improvements.

## Eligibility Criteria

The agent evaluates the following seven eligibility items:

1. **Property type:** Residential, commercial, and industrial properties can proceed. Agricultural property does not qualify.
2. **Ownership:** Sole and joint ownership can proceed if ownership is clearly recorded.
3. **Original property documents:** Original documents must be available.
4. **Loan amount:** The requested amount must be within ₹75,00,000, or the customer must accept an amount within that limit.
5. **Occupation and income mode:** The customer must be salaried or self-employed and receive income through a bank account rather than mainly in cash.
6. **Property market value:** The customer's approximate market-value estimate is recorded. Property value alone is not a disqualification.
7. **Repayment tenure:** The requested tenure must be between 3 and 15 years, inclusive.

## Conversation Flow

1. Verify customer identity.
2. Check whether the customer is available.
3. Introduce the offer and obtain consent.
4. Collect and validate eligibility information.
5. Disqualify, route the enquiry, or provide the initial qualification closing.

## Key Features

- One question at a time.
- Recognition of answers supplied out of order.
- Avoidance of unnecessary repeated questions.
- Handling of corrected or unclear answers.
- Immediate disqualification when a stated rule fails.
- Separate handling of existing property loans and EMI-reduction enquiries.
- No unsupported claims about guaranteed approval or completed callbacks.

## Repository Files

- `README.md` — Project overview.
- `system-prompt.md` — Complete system prompt.
- `test-cases.md` — Customer scripts and expected outcomes for 12 test scenarios.
- `testing-report.md` — Template for actual test results.
- `approach.md` — Implementation and testing approach.
- `improvements.md` — Prompt design decisions and version history.

## Testing

The test scenarios are documented in `test-cases.md`. Actual outcomes should be recorded in `testing-report.md` after each call is conducted.

Test cases must not be marked as passed until the recorded conversation has been checked against the expected behavior.

## Limitations

- The agent performs initial qualification only.
- Final approval and terms depend on a detailed assessment.
- No callback scheduler, CRM, lead-creation service, or specialist-notification integration is assumed to be connected.
- Customer-provided property values are estimates, not verified valuations.
- Interest rates, fees, credit thresholds, and approval timelines must not be invented.

## Author

Name: Chigullapally Yashwanth

## Submission Links

- Published agent: https://agent.retellai.com/orb/agent_4404182539bfdd00b3cf119a57?token=e6313c2809834e447f41e574b0665d88
- Screen recording: https://drive.google.com/file/d/1HT1cysW9GCTSCv4IBODEIp1ExsL54fW7/view?usp=sharing
