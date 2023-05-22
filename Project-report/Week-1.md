
- Learned about Tortoise SVN.
- Learned about Visual SVN server (local server). 
The thought process behind these two things to learn was to extract the data from “R - Revision 83941: /trunk/src/library/tools/po” and to store it in a database and create something like “R SVN build status/” containing only the details of translations.
After more exploration, I discovered that  “https://github.com/r-devel/translations” is already made, and “https://contributor.r-project.org/translations/#home” R-dashboard is already created.
To understand the above “https://github.com/r-devel/translations” code (mainly how is “https://github.com/r-devel/translations/blob/main/message_status.csv” created), I figured out “https://github.com/r-devel/rcontribution/tree/main/collaboration_campfires/translations” this GitHub page contains the code written most straightforward manner. 
After understanding the code, I figured out that GitHub actions are used for Continous Integration. GitHub Actions can automatically build, test, and deploy your code whenever changes are made to your repository. Even GitHub Actions are used to send notifications to the team members. 
I will learn more about GitHub Actions in the upcoming week.
