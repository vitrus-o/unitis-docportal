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

Project Homepage > Usecase > Voter Validation > Identity Verification

**Identity Verification**

The Identity Verification module secures the voting booth by authenticating the eligible student exclusively through their university-issued institutional email. It prompts the user to input the system-generated 6-digit One-Time Password (OTP) and validates it against a strict 5-minute expiration window to prevent unauthorized access. Upon successful verification, the system creates an ephemeral, secure voting session and grants the student immediate access to the ballot without requiring a persistent user account.

**Use Case Scenario**

| Use Case Name | Identity Verification |
|---------------|-----------------------------|
| **Summary**   | The system verifies the identity of the eligible voter by validating a time-sensitive code sent to their sole-owned institutional email. |
| **Actors**    | Student (Voter)            |
| **Preconditions** | The student has successfully passed Voter Eligibility Lookup and an active OTP exists in the system memory. |
| **Postconditions** | The system grants secure, ephemeral access to the E-Ballot module. |
| **Basic Flow** | **Actor Action** | **System Response** |
|               | 1. Enter the 6-digit OTP on the verification page and click "Authenticate". | 1.1. Validates that the entered OTP matches the generated code.<br>1.2. Confirms the code was entered within the 5-minute validity window.<br>1.3. Creates an active voting session and routes the user to the blind ballot. |
| **Exceptions** | 1. If the OTP is incorrect, the system clears the input fields and displays: "Invalid code. Please try again."<br>2. If the OTP is expired (past 5 minutes), the system requires the actor to request a new code and displays: "This code has expired for your security." |

----------------------------------------------------------