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

Project Homepage > Usecase > Election Results > View Public Results

**View Public Election Results**

The View Public Election Results module serves as the transparent, public-facing dashboard where VSU students and the general public can review the officially concluded election outcomes. It dynamically renders the cached tally data, displaying overall voter turnout, position winners, and detailed vote distributions through accessible graphical interfaces. Users can easily interact with the dashboard to filter results by specific faculties or positions, allowing them to analyze the data without putting any direct load on the secure voting database. 

**Use Case Scenario**

| Use Case Name | View Public Election Results |
|---------------|-------------------------------------|
| **Summary**   | Students and the general public access the event results to view the final vote counts and declared winners. |
| **Actors**    | Student, Public User   |
| **Preconditions** | The SEB Admin has successfully executed the "Publish Results" action. |
| **Postconditions** | The user successfully views the read-only, finalized election data. |
| **Basic Flow** | **Actor Action** | **System Response** |
|               | 1. Navigate to the event results page. | 1.1. Queries the event status to verify it is marked "Concluded".<br>1.2. Retrieves the cached, finalized tally data.<br>1.3. Renders the Results Dashboard, displaying total turnouts, position winners, and graphical vote distributions. |
|               | 2. Apply a filter (e.g., "View Faculty of Engineering Only"). | 2.1. Dynamically sorts and filters the displayed results on the screen based on the user's selection. |
| **Exceptions** | 1. If the user attempts to visit the URL before the SEB Admin has published the results, the system intercepts the request and displays a holding page: "Official results are currently being processed by the SEB and will be available shortly." |

----------------------------------------------------------
<p align="center">© 2026 Viribus</p>
