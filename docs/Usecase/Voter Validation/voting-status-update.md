# UNITIS

**Target:** UN.010.001

**Site Map**

[Project Homepage](/README.md)

[E-ballot](/docs/usecase/e-ballot.md)

[Voter Validation](/docs/usecase/voter-validation.md)

[Election Results](/docs/election-results.md)

[Result Archiving](/docs/result-archiving.md)

[Real-time Vote Count](/docs/real-time-vote-count.md)

[Candidate Applications](/docs/candidate-applications.md)

---

Project Homepage > Usecase > Voter Validation > Voting Status Update

**Voting Status Update**

The Voting Status Update module strictly enforces the "one student, one vote" rule by permanently modifying the voter's record the exact moment a ballot is cast. Operating entirely in the background, it locates the student's ID within the specific event masterlist and securely toggles their has_voted status from false to true. This automated update ensures absolute electoral integrity by instantly neutralizing any future login attempts with that same Student ID for the duration of the election.

**Use Case Scenario**

| Use Case Name | Voting Status Update |
|---------------|---------------------------|
| **Summary**   | The system finalizes the validation cycle by marking the student's name in the masterlist as "voted" immediately after their ballot is cast. |
| **Actors**    | System                    |
| **Preconditions** | The student has successfully finalized and submitted their ballot (via the E-Ballot module). |
| **Postconditions** | The student's record in the event masterlist is permanently updated to prevent future login attempts. |
| **Basic Flow** | **Actor Action** | **System Response** |
|               | 1. (Triggered automatically by ballot submission) | 1.1. Locates the specific Student ID in the active event masterlist.<br>1.2. Updates the has_voted boolean value from false to true.<br>1.3. Writes an entry to the Event Audit Log confirming the status change. |
| **Exceptions** | 1. If a database timeout occurs while attempting to update the status, the system retries the update. If it fails consecutively, it logs a critical error for the SEB Officer and Super Admin to manually review, ensuring the ballot is flagged for integrity checking. |

----------------------------------------------------------
<p align="center">© 2026 Viribus</p>