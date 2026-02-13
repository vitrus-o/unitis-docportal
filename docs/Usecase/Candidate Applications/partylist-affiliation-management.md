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

Project Homepage > Usecase > Candidate Applications > Partylist Affiliation Management

**Partylist Affiliation Management**

The Partylist Affiliation Management module grants registered party leaders the administrative authority to manage and verify their official candidate lineup. Operating within the authenticated portal, it allows partylist representatives to review incoming Certificates of Candidacy from students claiming affiliation with their specific group. Requiring approval before a candidate's party affiliation becomes official, the system prevents unauthorized students from falsely running under a party's banner.

**Use Case Scenario**

| Use Case Name | Partylist Affiliation Management |
|---------------|----------------------------------------|
| **Summary**   | The registered Partylist Representative reviews and explicitly confirms or denies candidates who have filed a Certificate of Candidacy claiming affiliation with their political party. |
| **Actors**    | Student (Partylist Representative) |
| **Preconditions** | The Partylist Representative is authenticated via the portal. A candidate has submitted a COC selecting this specific partylist. The election phase is still within the official filing period. |
| **Postconditions** | The candidate's political affiliation is officially verified and locked for the final SEB review, or the affiliation is rejected, reverting the candidate to an "Independent" status. |
| **Basic Flow** | **Actor Action** | **System Response** |
|               | 1. Navigate to the "Partylist Management" tab in the portal and view the list of pending affiliation requests. | 1.1. Retrieves and displays all candidate applications that selected this specific partylist during their COC filing. |
|               | 2. Click the "Confirm Affiliation" button next to a candidate's name. | 2.1. Updates the candidate's affiliation status in the database to "Verified".<br>2.2. Dispatches an automated email notification to the candidate confirming their official inclusion in the partylist lineup. |
| **Exceptions** | 1. If the Partylist Representative clicks "Reject Affiliation" (e.g., the candidate is not actually part of their official slate), the system automatically updates the candidate's affiliation to "Independent," sends a rejection notice to the candidate, and flags the change for the SEB Admin's final review. |

----------------------------------------------------------
<p align="center">© 2026 Viribus</p>
