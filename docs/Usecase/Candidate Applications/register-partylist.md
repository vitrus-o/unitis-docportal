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

Project Homepage > Usecase > Candidate Applications > Register Partylist

**Register Partylist**

The Register Partylist module empowers student leaders to formally establish their political coalitions within the election system before the core filing period begins. It securely captures essential partylist details, such as acronyms, platforms, and official logos. Once successfully registered, the system dynamically integrates the new partylist into the candidate application portal, allowing subsequent applicants to seamlessly affiliate their candidacy with the newly formed group.

**Use Case Scenario**

| Use Case Name | Register Partylist |
|---------------|---------------------------|
| **Summary**   | A student representative registers a formal partylist for the upcoming election, allowing subsequent candidates to officially affiliate with it during their application process. |
| **Actors**    | Student (Partylist Representative) |
| **Preconditions** | The election event is in the "Filing of Candidacy" phase. The student is authenticated. |
| **Postconditions** | The partylist is officially logged in the system and becomes available as a selectable affiliation for other candidates filing their applications. |
| **Basic Flow** | **Actor Action** | **System Response** |
|               | 1. Navigate to the "Partylist Registration" portal and enter the Partylist Name, Acronym, and platform details. | 1.1. Validates that the submitted acronym and name are unique and do not conflict with existing registrations for this specific Election_ID. |
|               | 2. Upload the required partylist logo and click "Register Partylist". | 2.1. Creates the partylist record in the database.<br>2.2. Dynamically populates the new partylist into the candidate affiliation dropdown menu. |
| **Exceptions** | 1. If a user attempts to register a partylist acronym that is already in use for the current election, the system highlights the input field and displays: "This partylist acronym is already registered for this event. Please choose a unique identifier." |

----------------------------------------------------------
<p align="center">© 2026 Viribus</p>
