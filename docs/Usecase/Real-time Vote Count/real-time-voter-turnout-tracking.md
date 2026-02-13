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

Project Homepage > Usecase > Real-time Vote Count > Real-Time Voter Turnout Tracking

**Real-Time Voter Turnout Tracking**

The Real-Time Voter Turnout Tracking module continuously monitors student participation during an active election without decrypting or tallying actual candidate selections. Operating securely in the background, it increments overall and demographic-specific turnout metrics, such as participation rates by faculty or department, the exact moment a ballot is successfully cast. This module ensures absolute election integrity while providing actionable, real-time data to help student leaders target underperforming demographics for voter mobilization.

**Use Case Scenario**

| Use Case Name | Real-Time Voter Turnout Tracking |
|---------------|----------------------------------------|
| **Summary**   | The system continuously calculates overall voter participation and demographic turnout statistics (e.g., by faculty or department) in the background to encourage voter engagement during the active election, without ever decrypting or aggregating candidate vote counts. |
| **Actors**    | System                    |
| **Preconditions** | The election event status is strictly set to "Active". Ballots are successfully passing the finalization stage. |
| **Postconditions** | The real-time cache is updated with the latest voter turnout metrics and demographic breakdowns, while actual candidate selections remain strictly uncounted until the official SEB canvassing period begins. |
| **Basic Flow** | **Actor Action** | **System Response** |
|               | 1. (Triggered automatically upon successful ballot submission from any voter in the system). | 1.1. Safely increments the overall voter turnout metric in a dedicated live-statistics table.<br>1.2. Increments the specific demographic turnout counter (e.g., "Faculty of Computing", "3rd Year Students") based on the voter's anonymized masterlist profile.<br>1.3. Pushes the updated turnout statistics payload to the live public dashboard cache. |
| **Exceptions** |

----------------------------------------------------------
<p align="center">© 2026 Viribus</p>
