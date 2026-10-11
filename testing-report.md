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

*Note: Session success figures are based on Retell AI's session outcome labels. Functional test verification is reported separately.*

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

These two sessions were marked unsuccessful by Retell AI because their recorded outcomes were unsuccessful and the end reason was user hangup. They are distinguished from the functional test results below.

## 4. Functional Test Status

All 12 functional test areas have been marked as verified following the functional testing of the voice agent.

| Test Area | Status |
|---|---|
| Customer identity verification | Verified |
| Availability and consent | Verified |
| Property type eligibility | Verified |
| Document availability | Verified |
| Income eligibility | Verified |
| Loan amount eligibility | Verified |
| Property ownership eligibility | Verified |
| Existing loan or EMI-reduction routing | Verified |
| Loan tenure eligibility | Verified |
| Out-of-order answers and corrections | Verified |
| Ambiguous customer responses | Verified |
| Correct closing and disqualification handling | Verified |

### Functional Testing Summary

- Customer identity verification and consent handling were tested.
- Property type, document availability, and ownership-related qualification flows were checked.
- Income, loan amount, and loan tenure eligibility handling were verified.
- Existing loan and EMI-reduction routing was checked.
- Out-of-order answers, corrections, and ambiguous responses were tested.
- Closing behavior, refusal handling, and customer disqualification flows were verified.

## 5. Observations

- Retell AI marked 13 out of 15 sessions as successful.
- Two sessions were marked unsuccessful and ended with a user hangup.
- Four sessions recorded positive sentiment; eleven recorded neutral sentiment.
- Average end-to-end latency was approximately 929 ms.
- Total recorded call cost was approximately $2.97.
- All 12 functional test areas are marked as verified.
- Platform session outcomes and functional correctness are tracked separately.

## 6. Improvements and Quality Assurance

1. Review unsuccessful session transcripts and recordings to identify possible conversation-flow issues.
2. Maintain the eligibility rules and verify them whenever the agent configuration changes.
3. Continue checking that ineligible customers receive an appropriate explanation and closing.
4. Monitor interruption handling and ambiguous responses.
5. Retest corrected and out-of-order answers after relevant changes.
6. Maintain a mapping between test scenarios and their corresponding call sessions.
7. Repeat functional tests after updates to ensure that previously verified behavior remains correct.

## 7. Conclusion

The Home Credit Loan Against Property qualification voice agent, named Priya, was evaluated using 15 web-call sessions on Retell AI.

The platform recorded 13 successful sessions and two unsuccessful sessions, giving a platform success rate of 86.7%. The total recorded call duration was 17 minutes and 49 seconds, the total cost was $2.971, and the average end-to-end latency was approximately 929 ms.

All 12 functional test areas are marked as verified, covering customer identity verification, consent, property eligibility, document availability, income and loan eligibility, ownership, existing loan routing, tenure, conversation corrections, ambiguous responses, and closing behavior.

The two unsuccessful platform sessions remain documented for quality assurance and improvement. Their outcomes do not, by themselves, establish a functional test failure.

**Report Status:** Functional test areas marked as verified; platform session results and quality assurance observations documented.
