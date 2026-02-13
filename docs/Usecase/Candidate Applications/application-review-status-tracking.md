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

Project Homepage > Usecase > Candidate Applications > Application Review & Status Tracking

**SEB Application Review & Status Tracking**

The SEB Application Review module provides the election board with a centralized dashboard to evaluate and process pending candidate applications. It displays the system's automated eligibility flags alongside the submitted documentary requirements, allowing administrators to make informed decisions quickly. Provides explicit justifications for rejected applications and automating email notifications for all status changes, this module ensures a transparent, auditable, and strictly governed candidate approval before the final E-Ballot is generated.

**Use Case Scenario**

| Use Case Name | SEB Application Review & Status Tracking |
|---------------|------------------------------------------------|
| **Summary**   | The SEB Admin reviews the pending candidate applications, assesses the system's automated eligibility flags, and officially updates the candidate's status to approve or reject their candidacy. |
| **Actors**    | SEB Admin                |
| **Preconditions** | Submitted candidate applications exist in the system with a "Pending" status. |
| **Postconditions** | The candidate's status is updated to "Approved" (pushing them to the official ballot) or "Rejected", and an automated notification is dispatched. |
| **Basic Flow** | **Actor Action** | **System Response** |
|               | 1. Navigate to the "Candidate Management Dashboard" and open a pending application. | 1.1. Retrieves the candidate's submitted documents, chosen partylist, and displays a prominent dashboard widget showing the system's automated SEB Code eligibility checks (e.g., GPA Check: Passed, Units Check: Passed). |
|               | 2. Click the "Approve Candidate" button to verify the application. | 2.1. Updates the candidate's tracking status from "Pending" to "Approved".<br>2.2. Automatically queues the candidate's profile and partylist data for rendering on the final E-Ballot.<br>2.3. Dispatches a status update email to the candidate. |
| **Exceptions** | 1. If the SEB Admin decides to click "Reject Candidate" (e.g., due to forged documents despite passing the automated data check), the system requires the admin to type a mandatory justification in a "Reason for Rejection" modal before the status can be successfully updated to "Rejected" and the notification sent. |

----------------------------------------------------------
<p align="center">© 2026 Viribus</p>
