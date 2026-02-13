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

Project Homepage > Usecase > Result Archiving > Historical Results Retrieval

**Historical Results Retrieval**

The Historical Results Retrieval module provides a transparent ledger where the student body can review the outcomes of past university elections. It queries the secure read-only archive to present aggregated data such as total turnouts, final vote distributions, and declared winners for any previously concluded event. Strictly serving anonymized tallies, this module ensures that historical transparency is maintained without ever compromising the strict privacy limits established during the actual voting process.

**Use Case Scenario**

| Use Case Name | Historical Results Retrieval |
|---------------|-------------------------------------|
| **Summary**   | Students or the general public access the archive portal to view the finalized tallies and winners of past university elections. |
| **Actors**    | Student, Public User   |
| **Preconditions** | The requested election has been formally archived. |
| **Postconditions** | The user successfully views the historical, read-only election data. |
| **Basic Flow** | **Actor Action** | **System Response** |
|               | 1. Navigate to the "Election Archives" portal and select a past event (e.g., "USSC 2024"). | 1.1. Queries the read-only historical database.<br>1.2. Retrieves the pre-computed tally data and overall turnout statistics. |
|               | 2. View the historical dashboard. | 2.1. Renders a read-only view of the position winners, party distributions, and total vote counts. |
| **Exceptions** | 1. If the user attempts to search for an Election_ID that does not exist or has not yet been officially transitioned to the "Archived" state by the SEB, the system displays: "Archive not found or currently unavailable."

----------------------------------------------------------
<p align="center">© 2026 Viribus</p>
