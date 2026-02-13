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

Project Homepage > Voter Validation

## Voter Validation Module

The Voter Validation module enforces strict eligibility checks and authentication protocols to ensure only registered, eligible students can access the voting system once per election. It combines masterlist lookups, institutional email verification, and automated status tracking to maintain electoral integrity throughout the voting period.

### Use Case Scenarios

- [Voter Eligibility Lookup](/docs/Usecase/Voter%20Validation/voter-eligibility-lookup.md)
- [Identity Verification (OTP Authentication)](/docs/Usecase/Voter%20Validation/identity-verification.md)
- [Voting Status Update](/docs/Usecase/Voter%20Validation/voting-status-update.md)

---

### Key Features

- **Masterlist Integration**: Real-time lookup against SEB-uploaded event masterlist
- **OTP Authentication**: Time-sensitive one-time password via institutional email
- **Duplicate Prevention**: Automatic `has_voted` flag to prevent multiple voting
- **Audit Logging**: Complete tracking of all validation events for integrity reviews
- **Session Security**: Ephemeral voting sessions with no persistent user accounts

----------------------------------------------------------
<p align="center">© 2026 Viribus</p>
