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

Project Homepage > Usecase > Election Results > Publish Results

**Publish Results**

The Publish Results module acts as the definitive control switch, allowing the SEB Admin to formally authorize the public release of the finalized election data. Upon confirmation, the system updates the global event status to "Concluded" and safely unlocks the results URL for the student body. It ensures that no election data is leaked prematurely by strictly guarding the routing logic until the official canvass has been fully vetted and approved by the board. This seamless transition guarantees a coordinated, official, and transparent announcement of the newly elected student leaders.

**Use Case Scenario**

| Use Case Name | Publish Results |
|---------------|------------------------|
| **Summary**   | The SEB Admin authorizes the public release of the finalized election outcomes to the student body and general public. |
| **Actors**    | SEB Admin             |
| **Preconditions** | The Official Canvass has been successfully generated and reviewed by the SEB Admin. |
| **Postconditions** | The election results are made visible on the event page and the event status is updated to "Concluded". |
| **Basic Flow** | **Actor Action** | **System Response** |
|               | 1. Click the "Publish Results to Public" button. | 1.1. Prompts the actor with a final confirmation modal (e.g., "Are you sure? This action will make the results visible to everyone."). |
|               | 2. Confirm publication. | 2.1. Changes the global Event Status to "Concluded".<br>2.2. Unlocks the /event/[ID]/results public route.<br>2.3. Triggers an automated email or system notification to all masterlist users that results are live (if configured). |
| **Exceptions** | 1. If a database synchronization error occurs during the status change, the system aborts the publication, keeps the route locked, and displays: "Error publishing results." |

----------------------------------------------------------
<p align="center">© 2026 Viribus</p>
