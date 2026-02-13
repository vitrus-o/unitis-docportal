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

Project Homepage > Usecase > Candidate Applications > File Certificate of Candidacy

**File Certificate of Candidacy (COC)**

The File Certificate of Candidacy module serves as the primary gateway for students to officially submit their applications for electoral positions, whether running independently or under a registered partylist. As the student selects their desired position, the system instantly cross-references their academic masterlist profile against strict SEB Code criteria, such as college jurisdiction and year level, to automatically block ineligible submissions. Upon successful upload of required documentary evidence, the application is securely routed to the administrative dashboard with a "Pending" status, providing the candidate with a timestamped tracking receipt for full transparency.

**Use Case Scenario**

| Use Case Name | File Certificate of Candidacy (COC) |
|---------------|-------------------------------------------|
| **Summary**   | A student submits their formal application to run for a specific electoral position, affiliating with a registered partylist or running as an independent, while the system automatically verifies their basic eligibility against the SEB Code. |
| **Actors**    | Student (Candidate)      |
| **Preconditions** | The election phase is "Filing of Candidacy". The student is authenticated and their academic masterlist data is available. |
| **Postconditions** | The application is securely stored with a "Pending" status, flagged with an automated eligibility assessment for the SEB Admin to review. |
| **Basic Flow** | **Actor Action** | **System Response** |
|               | 1. Select the target electoral position and choose a Partylist affiliation (or "Independent") from the dropdown. | 1.1. Evaluates the student's masterlist profile against the SEB Code criteria for the selected position (e.g., enrollment, grades). |
|               | 2. Upload the required documentary requirements (e.g., Certificate of Grades, Good Moral) and click "Submit Application". | 2.1. Generates an automated eligibility score (Pass/Fail flags for GPA, units, etc.).<br>2.2. Saves the application and uploaded documents to the database under a "Pending" status.<br>2.3. Provides the candidate with a timestamped tracking receipt. |
| **Exceptions** | 1. If the automated eligibility check detects a strict demographic mismatch based on the SEB Code (e.g., an Engineering student attempting to run for the Faculty of Computing Representative), the system disables the submission button and displays: "Ineligible: Your enrolled college does not match the jurisdiction of this position." |

----------------------------------------------------------
<p align="center">© 2026 Viribus</p>
