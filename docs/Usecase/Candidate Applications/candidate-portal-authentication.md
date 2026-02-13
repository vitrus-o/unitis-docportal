# UNITIS

**Target:** UN.010.001

**Site Map**

[Project Homepage](/README.md)

[E-ballot](/docs/usecase/e-ballot.md)

[Voter Validation](/docs/usecase/voter-validation.md)

[Election Results](/docs/usecase/election-results.md)

[Result Archiving](/docs/usecase/result-archiving.md)

[Real-time Vote Count](/docs/usecase/real-time-vote-count.md)

[Candidate Applications](/docs/usecase/candidate-applications.md)

---

Project Homepage > Usecase > Candidate Applications > Candidate Portal Authentication & Status Tracking

**Candidate Portal Authentication & Status Tracking**

The Candidate Portal Authentication module provides applicants with persistent, secure access to track their electoral journey using their official university Google account. By leveraging Google OAuth 2.0, the system ensures strict identity verification without the friction of separate passwords, allowing candidates to log in and view their dashboard. Once authenticated, candidates can monitor the real-time approval status of their Certificate of Candidacy, review their uploaded documentary requirements, and immediately read any official feedback or rejection justifications provided by the SEB Admin.

**Use Case Scenario**

| Use Case Name | Candidate Portal Authentication & Status Tracking |
|---------------|--------------------------------------------------------|
| **Summary**   | Candidates authenticate using their institutional Google account to access a personal dashboard where they can monitor the real-time approval status of their submitted Certificate of Candidacy (COC). |
| **Actors**    | Student (Candidate)      |
| **Preconditions** | The student has successfully submitted a candidate application. The student possesses a valid institutional Google account (@vsu.edu.ph). |
| **Postconditions** | The system grants access to a read-only dashboard displaying the candidate's current application status, submitted documents, and any SEB remarks. |
| **Basic Flow** | **Actor Action** | **System Response** |
|               | 1. Navigate to the Candidate Portal login page and click "Sign in with Google". | 1.1. Initializes the Google OAuth 2.0 flow and verifies the domain is a valid institutional email.<br>1.2. Cross-references the authenticated email against the Candidates database table. |
|               | 2. Select the specific Election Event. | 2.1. Retrieves the candidate's application record.<br>2.2. Renders the Candidate Dashboard highlighting the current status indicator (e.g., "Pending", "Approved", "Rejected") and any admin feedback. |
| **Exceptions** | 1. If the authenticated email does not match any existing candidate application in the database, the system restricts access to the dashboard and displays: "No pending or approved applications found for this email address. If you wish to run, please file a Certificate of Candidacy first."<br>2. If the user attempts to log in using a personal, non-institutional email address (e.g., @gmail.com), the system immediately rejects the OAuth token and displays: "Access Denied: Please use your official university email address to access the Candidate Portal." |

----------------------------------------------------------
<p align="center">© 2026 Viribus</p>
