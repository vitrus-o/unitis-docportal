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

Project Homepage > Usecase > Result Archiving > Event Archiving

**Event Archiving**

The Event Archiving module allows SEB Administrators to officially close the books on an election after the formal protest period has passed. Upon execution, the system locks the final tally, candidate profiles, and overall turnout metrics into a read-only historical state, preventing any further modifications. Crucially, it triggers an automated purge of the event's raw Voter Masterlist, safely deleting sensitive student identifiers from the active database to ensure long-term compliance with data privacy standards.

**Use Case Scenario**

| Use Case Name | Event Archiving |
|---------------|----------------------------|
| **Summary**   | The SEB Admin officially closes out the election, freezing the final tally and triggering the permanent deletion of the raw Voter Masterlist to protect student data. |
| **Actors**    | SEB Admin                 |
| **Preconditions** | The election results have been published, and any official appeal or protest period has expired. |
| **Postconditions** | The entire event (candidates and tally) is marked as "Archived," and sensitive student identifiers are purged from the database. |
| **Basic Flow** | **Actor Action** | **System Response** |
|               | 1. Click the "Archive Election" button on the Event Dashboard. | 1.1. Prompts for a final confirmation, warning that archiving will permanently delete the event's masterlist. |
|               | 2. Confirm archival. | 2.1. Changes the global event status from "Concluded" to "Archived".<br>2.2. Permanently drops the event's raw Voter Masterlist table, retaining only the aggregate turnout metrics (e.g., "Total Voted: 4,000"). |
| **Exceptions** | 1. If the admin attempts to archive an event that is still marked "Active" or "Draft," the system disables the action and displays: "Cannot archive an ongoing election." |

----------------------------------------------------------
<p align="center">© 2026 Viribus</p>
