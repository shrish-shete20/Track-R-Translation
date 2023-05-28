# Week 3: 21th May to 28th May 
- Added GitHub Action workflow to " https://github.com/shrish-shete20/translations " and " https://github.com/shrish-shete20/rcontribution-messages "
- Major time was spent on resolving errors in the workflow file.
- While writing the workflow file for " https://github.com/shrish-shete20/translations" , following were the concerns :
  - I was trying to make the file according to " https://github.com/RamiKrispin/deploy-flex-actions#set-automation-with-github-actions " ,but didn't work out.
  - Learnt about docker environment, but used runners instead of docker. It might be useful in future works. 
  - Error while installing packages : Even after installing packages according to this workflow file "https://github.com/shrish-shete20/translations/actions/runs/5085898885/workflow" ,some packages such as **tidyverse** and **plotly** didn't get installed properly showing this error " https://github.com/shrish-shete20/translations/actions/runs/5085898885/jobs/9139841760 " . Then learnt about adding dependencies commands in workflow file , adding DESCRIPTION file.
  - Github action workflow file was taking around 20 min to render, hence learnt about cache management and artifacts to reduce time.
- My thought and work process behind the re-rendering of the dashboard is as follows:
  - Firstly this translation_status.R "https://github.com/shrish-shete20/rcontribution-messages/blob/main/collaboration_campfires/translations/translation_status.R" should be run everyday which can be done using GitHub action.
  - Secondly, I changed the code in global_translation.R (https://github.com/shrish-shete20/translations/blob/main/global_translations.R), Rather than just copying the dataset made by "https://github.com/shrish-shete20/rcontribution-messages/blob/main/collaboration_campfires/translations/translation_status.R" use the link of raw csv file so, that if changes happen in the other repo can be seen here as well. Then, by using GitHub actions, we will re-render the dashboard every day, and a new HTML file will be generated; then, by using GitHub pages, we can deploy it on the dashboard or even we can use github actions again to deploy it.
- While writing the workflow file for " https://github.com/shrish-shete20/rcontribution-messages " , following were the concerns :
  - In "https://github.com/shrish-shete20/rcontribution-messages/blob/main/collaboration_campfires/translations/translation_status.R" file "with_dir(r_svn, system("git pull"))" changes the working repository (temporily) to r_svn repo. So while running the workflow file for the same "Error in setwd(dir = new) : cannot change working directory" error poped up . So need to do some minor changes in "https://github.com/shrish-shete20/rcontribution-messages/blob/main/collaboration_campfires/translations/translation_status.R" file and learnt how to checkout multiple repository(side by side and even nested). I tried to do these stuffs on "https://github.com/shrish-shete20/trying" repo.
  - Did some minor changes in the translation_status.R file (removed some libraries functions and added new ones).(ex:Added this text "txt <- iconv(txt, from = "UTF-8")" for encoding the translations).
  - Recent error which I wasn't able to resolve in this week : **get_message_status** function works properly in Rstudio but while running the Rscript in Github action workflow it shows error :-  Error in `pmap()`:
ℹ In index: 13.
Caused by error in `tibble()`:
! Tibble columns must have compatible sizes.
• Size 583: Existing data.
• Size 69: Column `translated`.
