# UNITIS

**Target:** UN.010.001

**Site Map**

[Project Homepage](/README.md)

[E-ballot](/docs/Usecase/e-ballot.md)

[Voter Validation](/docs/Usecase/voter-validation.md)

[Election Results](/docs/election-results.md)

[Result Archiving](/docs/result-archiving.md)

[Real-time Vote Count](/docs/real-time-vote-count.md)

[Candidate Applications](/docs/candidate-applications.md)

---

Project Homepage > Usecase > Voter Validation > Voter Eligibility Lookup

**Voter Eligibility Lookup**

The Voter Eligibility Lookup module serves as the initial security checkpoint for the election, automatically cross-referencing a student's ID against the official event masterlist uploaded by the SEB. It acts as an automated attendance checker by ensuring the student is registered for the specific Election_ID and validating that their has_voted status is currently false. Once eligibility is confirmed, this module seamlessly triggers the generation of a secure, time-sensitive access code to begin the multi-factor authentication process.

**Use Case Scenario**

| Use Case Name | Voter Eligibility Lookup |
|---------------|-------------------------------|
| **Summary**   | The system performs an attendance check by looking up the student's ID in the event masterlist to verify they are eligible and have not yet voted. |
| **Actors**    | Student (Voter)              |
| **Preconditions** | The SEB has uploaded the official masterlist for the current Election_ID. The election is currently within the active voting period. |
| **Postconditions** | The system confirms eligibility and initiates the OTP verification sequence via the student's institutional email. |
| **Basic Flow** | **Actor Action** | **System Response** |
|               | 1. Enter Student ID on the event login page and click "Verify Eligibility". | 1.1. Queries the database to look up the ID within the specific event's masterlist.<br>1.2. Verifies the has_voted flag is currently set to false.<br>1.3. Generates a secure OTP and emails it to the associated institutional email address. |
| **Exceptions** | 1. If the Student ID is not found in the masterlist, the system displays an error: "Your ID is not registered for this specific election event."<br>2. If the Student ID is found but the has_voted flag is true, the system halts the login and displays: "A ballot has already been cast using this Student ID." |

----------------------------------------------------------
<p align="center">© 2026 Viribus</p>