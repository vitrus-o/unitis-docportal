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

Project Homepage > Usecase > Election Results > Generate Official Canvass

**Generate Official Canvass**

The Generate Official Canvass module provides SEB Administrators with a secure, automated tool to calculate final vote counts strictly after an election's polls have closed. It aggregates all encrypted ballot records from the database to accurately determine the winners based on established rules. To ensure absolute transparency and auditability, the system automatically generates a timestamped, digitally signed PDF report of the final tally. This certified document serves as the official, immutable record of the election outcomes before any public announcement is made.

**Use Case Scenario**

| Use Case Name | Generate Official Canvass |
|---------------|---------------------------------------------|
| **Summary**   | The system securely aggregates the cast ballots to determine the final vote counts and generates a certified, official report. |
| **Actors**    | SEB Admin                     |
| **Preconditions** | The voting period has officially ended. The SEB Admin has manually set the Election Status to "Closed" to prevent any further ballots from being cast. |
| **Postconditions** | The system computes the final vote counts, identifies the winners, and readies the certified PDF report. |
| **Basic Flow** | **Actor Action** | **System Response** |
|               | 1. Navigate to the Event Dashboard and click "Generate Official Tally". | 1.1. Validates that the election status is strictly "Closed".<br>1.2. Cryptographically aggregates all ballot records from the database.<br>1.3. Displays the finalized tally interface with candidates ranked by vote count. |
|               | 2. Click "Download Certified Canvass Report". | 2.1. Generates a non-editable PDF document containing the final counts, timestamped and digitally signed by the system. |
| **Exceptions** | 1. If the actor attempts to generate the tally while the election is still marked "Active" or "Draft", the system disables the button and displays an error: "Cannot generate tally: Polls are still open." |

----------------------------------------------------------
<p align="center">© 2026 Viribus</p>
