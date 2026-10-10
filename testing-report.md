# Testing Report — Home Credit Voice Agent

## 1. Project Overview

- **Project:** Home Credit Loan Against Property (LAP) Qualification Voice Agent
- **Agent Name:** Priya
- **Platform:** Retell AI
- **Testing Date:** October 10, 2026
- **Channel:** Web Call
- **Total Call Sessions:** 15

## 2. Call Session Summary

| Metric | Result |
|---|---:|
| Total calls | 15 |
| Successful sessions | 13 |
| Unsuccessful sessions | 2 |
| Platform success rate | 86.7% |
| Total call duration | 17 minutes 49 seconds |
| Total cost | $2.971 |
| Average end-to-end latency | Approximately 929 ms |
| Positive sentiment | 4 calls |
| Neutral sentiment | 11 calls |

*Note: These success figures are based on Retell AI's session outcome labels. They do not independently verify that all qualification rules were followed.*

## 3. Unsuccessful Sessions

### Session 1

- **Time:** October 10, 2026, 12:44:11 PM
- **Session ID:** `call_0cec57d2d32de99dd401d90cf27`
- **Duration:** 15 seconds
- **End Reason:** User hangup
- **Outcome:** Unsuccessful
- **End-to-End Latency:** 1027 ms

### Session 2

- **Time:** October 10, 2026, 11:49:41 AM
- **Session ID:** `call_d3ee6679a7590cd75996a7e0007`
- **Duration:** 26 seconds
- **End Reason:** User hangup
- **Outcome:** Unsuccessful
- **End-to-End Latency:** 820 ms

These sessions should be reviewed to determine whether the caller ended the call early or the agent failed to handle the conversation correctly.

## 4. Functional Test Status

The summary logs do not show which test scenario was performed in each call. Therefore, individual scenario results have not yet been confirmed.

| Test Area | Status |
|---|---|
| Customer identity verification | Not yet verified |
| Availability and consent | Not yet verified |
| Property type eligibility | Not yet verified |
| Document availability | Not yet verified |
| Income eligibility | Not yet verified |
| Loan amount eligibility | Not yet verified |
| Property ownership eligibility | Not yet verified |
| Existing loan or EMI-reduction routing | Not yet verified |
| Loan tenure eligibility | Not yet verified |
| Out-of-order answers and corrections | Not yet verified |
| Ambiguous customer responses | Not yet verified |
| Correct closing and disqualification handling | Not yet verified |

## 5. Observations

- Retell AI marked 13 out of 15 sessions as successful.
- Two sessions were marked unsuccessful and ended with a user hangup.
- Four sessions recorded positive sentiment; eleven recorded neutral sentiment.
- Average end-to-end latency was approximately 929 ms.
- Total recorded call cost was approximately $2.97.

## 6. Planned Improvements

1. Review the transcripts and recordings of unsuccessful sessions.
2. Verify that all eligibility conditions are correctly applied.
3. Check that ineligible customers receive the correct explanation and closing.
4. Test interruption handling and ambiguous responses.
5. Verify the handling of corrected and out-of-order answers.
6. Map each call to its actual test scenario.
7. Retest any issues and update the results.

## 7. Conclusion

The initial call logs provide an overview of the voice agent's performance across 15 web-call sessions. Retell AI recorded 13 successful outcomes and two unsuccessful outcomes, with a total cost of approximately $2.97 and average end-to-end latency of approximately 929 ms.

Transcript review and scenario-based testing are still required to confirm functional correctness.

**Report Status:** Initial call summary completed; scenario-level verification pending.
