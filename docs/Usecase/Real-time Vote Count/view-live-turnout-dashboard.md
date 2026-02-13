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

Project Homepage > Usecase > Real-time Vote Count > View Live Turnout Dashboard

**View Live Turnout Dashboard**

The Live Turnout Dashboard serves as an auto-refreshing interface that displays ongoing voter participation statistics to the student body and faculty. Instead of revealing candidate standings, it utilizes dynamic charts and graphs to highlight turnout percentages across different university populations, instantly reflecting the data pushed from the real-time tracking module. This strategic visibility empowers the campus community to actively encourage peers in low-turnout sectors to vote, fostering a more engaged and representative electoral process without compromising the secrecy of the final canvass.

**Use Case Scenario**

| Use Case Name | View Live Turnout Dashboard |
|---------------|--------------------------------------|
| **Summary**   | Students and the public access a live-updating web dashboard to monitor the unofficial, real-time vote counts and turnout statistics while the election is ongoing. |
| **Actors**    | Student, Public User   |
| **Preconditions** | The election event status is "Active". |
| **Postconditions** | The user views the most current, auto-refreshing tally without having to manually reload the page. |
| **Basic Flow** | **Actor Action** | **System Response** |
|               | 1. Navigate to the live event turnout dashboard.
|               | 2. Remain on the page as new votes are cast across the university. 
| **Exceptions** | 1. If the SEB Admin changes the election status to "Closed," the system severs the live data stream, freezes the dashboard numbers, and displays a prominent banner: "Polls Closed. Awaiting Official SEB Canvass."<br>2. If the user loses internet connectivity, the system detects the dropped connection and displays a warning overlay: "Live connection lost. Attempting to reconnect..." to prevent them from looking at outdated numbers. |

----------------------------------------------------------
<p align="center">© 2026 Viribus</p>
