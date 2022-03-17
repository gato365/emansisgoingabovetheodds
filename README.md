# emansisgoingabovetheodds
My project Website


Important Terminology 
  - blogdwn? - website platform (i.e., Wordpress)
  - hugo? - static site generator
  - Netlify? - web development platform
  - GitHub - version control (Google Doc) & Sharing
      - Commit - 
      - Push -
      - Pull - 
      
  - YAML

Prerequisites
*Good*  - Install a recent version of R and RStudio 
*Mine*  - Create a GitHub account (use jamesijw23@gmail.com)
*Dont Know*  - Connect RStudio to GitHub (preferably with HTTPS)
*Create a new one*- Sign up with Netlify using your GitHub account


Resources for getting started with GitHub 
https://happygitwithr.com/github-acct.html
https://the-turing-way.netlify.app/collaboration/github-novice.html#
https://www.startyourlab.com/docs/github-accounts/

## Good Example
https://www.kelly-bodwin.com/
https://shilaan.rbind.io/post/building-your-website-using-r-blogdown/




## Set Up First GitHub



##---------------
## GitHub Setup
##---------------
Step 1: Create a GitHub account with the same email that you use for R Studio cloud
https://github.com/hadley
https://github.com/devoncarew
Step 2: Create a new Repository and name it something regarding your name and your blog
✓ Keep the repository Public
✓ Add a README file
✓ **Do not add .gitignore**
You can choose MIT License






##---------------
## Setting Up Github Repository 1st time
##---------------
☞︎ Go to https://github.com/your-username/your-repository
☞︎ Click on the green Code button
☞ Copy the HTTPS link to your clipboard

Step 4: Click on the New Project then within R Studio Cloud
Step 5: Click on New Project from Git Repository
Step 6: Paste  https://github.com/your-username/your-repository where it says "URL for your Git Repository"
Click OK


##---------------
## Save 1st file and committing it to GitHub
##---------------

Create a R markdown file and delete content
create a histogram of mpg from the mtcars data frame
Save the file as test_markdown
Click on the Git Symbol in the middle of the screen
Click Commit
CLick on the box new the yellow M 
then type notes on what you ncreated in the box next to it
then click commit
press OK 
then click push (*More steps*: Settings - Tokens - Generate Tokens - Set date - copy token save in a good location)
Go to GitHub and view the change
erase the code regarding the histogram and plot a scatter plot between mpg and wt within mtcars
Save file
Follow the process to commit and push.
Now click on pull and you can see both versions of the code you created



##---------------
## Website Creation
##---------------




Step 3: Create website with {blogdown}
install.packages("blogdown") # install the blogdown package
library(blogdown) # load blogdown
new_site(theme = "wowchemy/starter-academic") # create your website!
1-2 pop screens will show up, just hit 'Save'
hit no to preview website



##---------------
## Working with github
##---------------

Step 4: Push ⬆︎ to GitHub
Run the following code in the console: file.edit("gitignore")
Copy and paste the following code into the gitignore file:
First Set run
.Rproj.user
.Rhistory
.RData
.Ruserdata
.DS_Store

blogdown::check_site()

Then add these to gitignore file
Thumbs.db
/public/
/resources/
.hugo_build.lock




Before we make our first commit, we use blogdown to check all our files:

blogdown::check_site()
Two boxes come up click save twice


options(blogdown.hugo.version = "0.93.3")

    


Step 5: Deploy site with Netlify
Go to Netlify and sign up using your github profile
netlify.com
Click on Sites
Click on Add New Sites
Click on Import an Existing Project
Click on GitHub and it should link up
Click on the repository that connects to your repository
Scroll down on the next page to Deploy Site
Wait for Deploy bots
Click Custom Domain





Back in RStudio, change the baseurl to your new link in your configuration file:

install.packages("rstudioapi")
library(rstudioapi) # to easily navigate to files
rstudioapi::navigateToFile("config.yaml") OR
Go to the config folder click default, open config.yaml
Do a control find for 'baseurl' and remove 'https://academic-demo.netlify.app/' and add your website name in quotes

do a check - blogdown::check_site()


Double check HUGO locally and the version by Netlify  are  the same version  
make sure that the version of Hugo that you are using locally with {blogdown} matches the version used by Netlify (which is specified in netlify.toml). You will likely need to change your netlify.toml file.
rstudioapi::navigateToFile("netlify.toml") 
    
    
Step 6: Customize your site with Wowchemy 🎨
    
    
Change Contact page:
The core parameters for the website can be edited in the config/_default/params.yaml file.

Change the Menu:
The main menu links in the navigation bar can be edited in the config/_default/menu.yaml file.

Personal information
Widgets
Menu
Theme
Website icon
Step 7: Write your first post ✍
We’re done! 💪
        Acknowledgements