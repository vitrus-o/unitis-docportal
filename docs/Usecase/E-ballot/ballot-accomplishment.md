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

Project Homepage > Usecase > E-ballot > Ballot Accomplishment

**Ballot Accomplishment**

The Ballot Accomplishment module governs the interactive user interface where an authenticated student actively makes their electoral choices. It presents the candidate names and party affiliations while strictly enforcing position-specific rules, such as maximum selection limits or abstentions. As the user navigates the ballot, the system temporarily stores their choices and provides real-time progress tracking to ensure all constraints are met before proceeding to the review stage.

**Use Case Scenario**

| Use Case Name | Ballot Accomplishment |
|---------------|-----------------------------|
| **Summary**   | The process of a student interacting with the digital ballot to select their preferred candidates according to position rules. |
| **Actors**    | Student (Voter)            |
| **Preconditions** | The student has successfully authenticated (UR2) and holds an active session for the specific Election_ID. |
| **Postconditions** | The system temporarily stores the user's candidate selections in the local state, ready for final review. |
| **Basic Flow** | **Actor Action** | **System Response** |
|               | 1. Scroll through the ballot and view the electoral positions and candidates. | 1.1. Renders the blind ballot UI (names, photos, and parties) and enforces selection limits for each position header. |
|               | 2. Click on a candidate's row or an "Abstain" option. | 2.1. Highlights the selected row.<br>2.2. Updates the real-time progress tracker in the floating footer. |
|               | 3. Click the "Review Ballot" button. | 3.1. Aggregates all current selections.<br>3.2. Triggers and populates the Review Modal. |
| **Exceptions** | 1. If the actor attempts to select a candidate when the maximum limit for that position (e.g., "Vote for 6") is already reached, the system prevents the selection and briefly displays a warning UI prompt: "Maximum limit reached for this position." |

----------------------------------------------------------
<p align="center">© 2026 Viribus</p>