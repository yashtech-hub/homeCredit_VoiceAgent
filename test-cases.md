# Test Cases — Home Credit  Voice Agent

## Instructions

Run each test as a separate call. Start with the identity verification and consent steps. Speak the customer responses naturally, one at a time.

Record the actual outcome and evidence link in `testing-report.md`. Mark a test as passed only after checking the conversation or transcript.

## Test 1: Successful Qualification

**Customer responses**
1. "Yes, this is Rahul Sharma. I can talk now."
2. "Yes, that's fine."
3. "It's a residential property, and I'm the sole owner."
4. "Yes, I have the original property documents available."
5. "I'm looking for fifty lakh rupees."
6. "I'm salaried, and my salary comes into my bank account."
7. "The property is worth approximately one crore rupees."
8. "I'd prefer a repayment tenure of ten years."

**Expected result:** The agent records all seven items, asks no unnecessary repeated questions, gives the initial qualification closing, and ends the call. The closing must clarify that final approval depends on further assessment.

## Test 2: Agricultural Property

**Customer responses**
1. "Yes, this is Rahul Sharma. I can talk now."
2. "Yes, that's fine."
3. "The property I want to use is agricultural land."

**Expected result:** Immediate disqualification after the property type is identified. The agent must not ask the remaining eligibility questions.

## Test 3: Original Documents Unavailable

**Customer responses**
1. "Yes, this is Rahul Sharma. I can talk now."
2. "Yes, that's fine."
3. "It's a residential property, and I'm the sole owner."
4. "No, I don't have the original property documents available."

**Expected result:** Immediate disqualification after the customer confirms the documents are unavailable.

## Test 4: Income Mainly Received in Cash

**Customer responses**
1. "Yes, this is Rahul Sharma. I can talk now."
2. "Yes, that's fine."
3. "It's a commercial property, jointly owned with my brother."
4. "Yes, the original property documents are available."
5. "I'm looking for thirty lakh rupees."
6. "I'm self-employed, and most of my income is received in cash."

**Expected result:** The agent identifies the cash-income rule and disqualifies the customer without asking about property value or tenure.

## Test 5: Amount Above the Maximum, Customer Accepts a Lower Amount

**Customer responses**
1. "Yes, this is Rahul Sharma. I can talk now."
2. "Yes, that's fine."
3. "It's a residential property, and I'm the sole owner."
4. "The original property documents are available."
5. "I initially wanted ninety lakh rupees, but I could consider seventy lakh."
6. "I'm salaried, and my salary comes into my bank account."
7. "The property is worth about one crore twenty lakh rupees."
8. "I'd prefer a twelve-year repayment tenure."

**Expected result:** The agent records ₹70,00,000 as the amount the customer is willing to consider, continues with the remaining items, and gives the qualified closing only if all required criteria pass. It must not automatically replace the accepted amount with ₹75,00,000.

## Test 6: Joint Ownership

**Customer responses**
1. "Yes, this is Rahul Sharma. I can talk now."
2. "Yes, that's fine."
3. "It's a residential property jointly owned by my wife and me."
4. "Yes, the original property documents are available."
5. "I'm looking for forty lakh rupees."
6. "I'm salaried, and my income comes into my bank account."
7. "The property is worth around ninety lakh rupees."
8. "I'd prefer an eight-year repayment tenure."

**Expected result:** The agent accepts joint ownership and does not disqualify the customer solely for that reason. It qualifies only if all seven eligibility items pass.

## Test 7: Existing Property Loan or EMI Reduction

**Customer responses**
1. "Yes, this is Rahul Sharma. I can talk now."
2. "Yes, that's fine."
3. "I already have a loan against this property, and I'd like to reduce my EMI."

**Expected result:** The agent stops the standard questionnaire, gives the loan-transfer/EMI-reduction response, and ends the call. It must not claim a specialist has actually been notified.

## Test 8: Customer Is Busy

**Customer responses**
1. "Yes, this is Rahul Sharma, but I'm in a meeting right now."
2. "Tomorrow morning, around ten AM, would be convenient."

**Expected result:** The agent does not ask eligibility questions. It records the customer's preferred callback time, thanks the customer, and ends the call without claiming the callback is scheduled.

## Test 9: Customer Refuses an Eligible Tenure

**Customer responses**
1. "Yes, this is Rahul Sharma. I can talk now."
2. "Yes, that's fine."
3. "It's a residential property, and I'm the sole owner."
4. "Yes, the original property documents are available."
5. "I'm looking for twenty-five lakh rupees."
6. "I'm salaried, and my salary comes into my bank account."
7. "The property is worth around seventy lakh rupees."
8. "I only want a two-year repayment period. I don't want a longer tenure."
9. If asked whether they would consider a tenure from three to fifteen years: "No, I don't want a longer tenure."

**Expected result:** The agent explains the permitted tenure range. After the customer declines to consider an eligible tenure, it disqualifies and ends the call.

## Test 10: Answers Given Out of Order

**Customer responses**
1. "Yes, this is Rahul Sharma. I can talk now."
2. "Yes, that's fine."
3. "It's a residential property worth around one crore twenty lakh rupees. It's jointly owned by my wife and me, and I need sixty lakh rupees for ten years."
4. "Yes, the original documents are available."
5. "I'm self-employed, and my income comes into my bank account."

**Expected result:** The agent records property type, market value, ownership, amount, tenure, document availability, occupation, and income mode. It asks only for information genuinely missing and gives the qualified closing only if every required item passes.

## Test 11: Ambiguous Document Availability

**Customer responses**
1. "Yes, this is Rahul Sharma. I can talk now."
2. "Yes, that's fine."
3. "It's a commercial property, and I'm the sole owner."
4. "I think the original papers are somewhere at home, but I'm not sure if they're available."

**Expected result:** The agent asks whether the original documents are available now. It must not assume that they are available. If the customer cannot clarify, the agent must not give the qualified closing.

## Test 12: Customer Corrects an Earlier Answer

**Customer responses**
1. "Yes, this is Rahul Sharma. I can talk now."
2. "Yes, that's fine."
3. "It's a residential property—actually, sorry, I mean agricultural land."

**Expected result:** The agent uses the latest clear answer, identifies agricultural property, and immediately disqualifies the customer without continuing the questionnaire.

## Additional Recommended Tests

If time permits, test the following behaviors too:

- The customer refuses identity verification.
- The customer declines consent.
- The customer asks to end the call.
- The customer asks about an interest rate or fee not specified in the prompt.
- The customer asks the agent to hold.
- The customer speaks another language.
- The customer gives an amount in lakhs or crores.
- The customer provides an unclear ownership arrangement.

## Acceptance Criteria

A test passes only if the actual agent behavior matches the expected result. Document failures and retest after making prompt changes.
