# UNITIS
**Target:** UN.010.001

**Site Map**

[Project Homepage](/README.md)

[E-ballot](/docs/Usecase/e-ballot.md)

[Voter Validation](/docs/Usecase/voter-validation.md)

[Election Results](/docs/Usecase/election-results.md)

[Result Archiving](/docs/Usecase/result-archiving.md)

[Real-time Vote Count](/docs/Usecase/real-time-vote-count.md)

[Candidate Applications](/docs/Usecase/candidate-applications.md)

---

Project Homepage > Usecase > E-ballot > Ballot Finalization

**Ballot Finalization**

The Ballot Finalization module handles the secure review and permanent submission of the user's accomplished ballot into the database. It prompts the voter with a comprehensive, read-only summary of their selections, highlighting any undervoted positions, and requires a final manual confirmation to prevent accidental submissions. Once confirmed, the system cryptographically records the vote, updates the masterlist to permanently prevent duplicate voting, and issues an anonymized transaction receipt to the student.

**Use Case Scenario**

| Use Case Name | Ballot Finalization |
|---------------|---------------------------|
| **Summary**   | The review and official submission of the accomplished ballot into the secure database. |
| **Actors**    | Student (Voter)          |
| **Preconditions** | The student has accomplished the ballot and the Review Modal is currently active on their screen. |
| **Postconditions** | The vote is permanently recorded, the student is marked as "Voted" in the masterlist, and the active session is terminated. |
| **Basic Flow** | **Actor Action** | **System Response** |
|               | 1. Review the summary list of selected candidates on the modal. | 1.1. Displays a read-only summary list.<br>1.2. Highlights any undervoted positions with a warning indicator (e.g., "You selected 8/12"). |
|               | 2. Click the "Confirm & Submit Vote" button. | 2.1. Cryptographically inserts the ballot record into the database.<br>2.2. Updates the actor's record in the Event Masterlist to has_voted: true.<br>2.3. Generates an anonymized Transaction ID.<br>2.4. Redirects the actor to the Vote Success/Receipt page. |
| **Exceptions** | 1. If the actor clicks the "Edit Choices" button instead of confirm, the system closes the Review Modal and returns focus to the active ballot without losing any previous selections.<br>2. If a network or database error occurs exactly during submission (Step 2.1), the system halts the process, prevents the has_voted flag from being updated, and displays a critical error message advising the student to try again or contact the SEB. |

----------------------------------------------------------
<p align="center">© 2026 Viribus</p>