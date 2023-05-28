# Week 3: 21th May to 28th May 
- Added GitHub Action workflow to " https://github.com/shrish-shete20/translations " and " https://github.com/shrish-shete20/rcontribution-messages "
- Major time was spent on resolving errors in the workflow file.
- While writing the workflow file for " https://github.com/shrish-shete20/translations" , following were the concerns :
  - I was trying to make the file according to " https://github.com/RamiKrispin/deploy-flex-actions#set-automation-with-github-actions " ,but didn't work out.
  - Learnt about docker environment, but used runners instead of docker. It might be useful in future works. 
  - Error while installing packages : Even after installing packages according to this workflow file "https://github.com/shrish-shete20/translations/actions/runs/5085898885/workflow" ,some packages such as **tidyverse** and **plotly** didn't get installed properly showing this error " https://github.com/shrish-shete20/translations/actions/runs/5085898885/jobs/9139841760 " . Then learnt about adding dependencies commands in workflow file , adding DESCRIPTION file.
  - Github action workflow file was taking around 20 min to render, hence learnt about cache management and artifacts to reduce time.
  -   
