BUNDLE ONE
 
Yves-Tabor edited this page last week · 2 revisions
# Exercise 1:
Question:

Create a project folder & initialize git
Make changes to the project (add files and contents)
Rename your main branch from master to main (If your branch name is already main then rename it to master and then back to main)
Stage your changes and commit them
Create a Github repo and connect it with your project
Push your changes to GitHub
Create a new branch dev
From dev create another branch test
Go back to the dev branch and delete the test branch
Git Process:

.Create and enter your project folder, then initialize Git: mkdir my-project cd my-project git init

. Add some files and content: You can add manually or use the "echo" command to add files and add some contents at the same time echo "# My Project" > README.md echo "console.log('Hello, Git!');" > app.js

. Rename the branch from master to main (or simulate the renaming).: git branch -M master git branch -M main

. Stage and commit your changes.git add : git commit -m "Initial commit"

. Connect your local repo to the remote GitHub repo. : git remote add origin https://github.com/your-username/my-project.git git push -u origin main - To push your local main branch to GitHub.

. Create a dev branch, then from there create a test branch : git checkout -b dev git checkout -b test

. Switch back to dev and delete the test branch : git checkout dev git branch -d test

# Exercise 2:
Question:

Create a new home.html file, add some html changes and save them
Stash save your current changes
Repeat the same process for a new about.html page and stash save your changes
Repeat the same process for a new team.html page and stash save your changes
Using stash pop restore the changes of the about.html page
With the help of an index use stash pop bring back the home.html page changes
Commit the current changes and push them
Using stash pop restore the changes of the team.html page index
Reset the current changes using git reset and go back to the changes without the team.html page
Git Process:

.Creates a new file home.html with basic HTML content and then : git stash push -m "home.html changes" : stashes the current changes and labels the stash with a message.

Creates a new file about.html with some content and again: git stash push -m "about.html changes"

Creates a new file team.html with some content and once lastly: git stash push -m "team.html changes"

. git stash list: Lists all saved stashes to identify the index for about.html. git stash pop stash@{1}: Restores the stash that contains about.html changes. Index may vary depending on order — use list to confirm. git stash pop stash@{2}: Restores the stash that contains home.html changes (again, confirm index from stash list).

git add . git commit -m "Restored home.html and about.html" : Stages and commits the restored changes. git push: Pushes the committed changes to the remote repo.

git stash pop stash@{0} : Restores the stash for team.html. Make sure index is correct based on stash list.

git reset --hard HEAD: Resets working directory to the last commit — discards team.html and any unstaged changes.

END OF FIRST BUNDLE

*************************************************************************************************************************************

BUNDLE TWO
 
Yves-Tabor edited this page last week · 3 revisions
# Exercise 1 :
Question :

Create a new branch named ft/bundle-2
Add new changes to your project. create a new page named services.html and add some changes
Commit your changes and create a Pull Request against the main branch in your github repository
Request a review and make sure your Pull request gets merged (Look for someone to merge your PR)
Git Process :

. git checkout -b ft/bundle-2 : Creates and switches to a new branch named ft/bundle-2. echo "

<title>Document</title>
This is the Second bundle
" > services.html All this echo command has to be at the same line, and we are creating a new file named services.html with some basic HTML content.
. git add . git commit -m "Add services.html page" : Stages and commits the new file with a message. git push -u origin ft/bundle-2 : Pushes the new branch and sets it to track the remote branch.

Now we can go to GitHub and create a Pull Request (PR) from ft/bundle-2 to main. In the PR, use the “Request review” feature to ask someone to review your code. Once someone reviews and approves, ask them to merge the Pull Request.

# Exercise 2 :
Question :

Checkout your main branch and pull the latest changes
Create a new branch named ft/service-redesign
Add new changes to the service.html page
commit and push them
create a new PR for your changes
go back to your main branch and add again new changes to your service.html page, you can add different changes but make sure to affect the same part(line of code) as you did in the other PR
Commit and push those changes
Now go back to the Github PR you had created for the ft/service-redesignbranch, you will then see that you have conflicts with the main branch
In your project checkout the ft/service-redesignbranch
Compare the ft/service-redesignwith the main branch using git diff and observe the changes
Using git merge, merge the main branch with ft/service-redesign branch and commit and push you changes again
Git Process : . git checkout main : Switches to the main branch.

git pull origin main : Pulls the latest changes from the remote main branch to ensure it's up to date.

git checkout -b ft/service-redesign : Creates and switches to a new branch named ft/service-redesign.

echo "

Redesigned services section goes here.

" >> services.html : Adds new content to services.html (simulate the redesign).
.To stage and commit the changes made in services.html: git add services.html git commit -m "Redesign services section in services.html"

git push -u origin ft/service-redesign : Pushes the new branch to the remote and sets the upstream. Now we can go to GitHub and create a Pull Request (PR) from ft/service-redesign into main . git checkout main : Switches back to the main branch.

echo "

Minor update to services section in main branch.

" >> services.html : Adds a different change to the same line or section of services.html as the other PR to simulate a conflict.
.Commits the conflicting change on main: git add services.html git commit -m "Update same part of services.html from main" git push origin main : Pushes the new changes to the main branch.

.Let's now go back to the PR on GitHub for ft/service-redesign — it will show a conflict with main.

git checkout ft/service-redesign : Switches back to the feature branch.

git diff main : Compares the current branch with main to view differences — useful to understand the conflict.

git merge main : Merges the latest changes from main into ft/service-redesign — this will trigger a merge conflict.

.Manually resolve the merge conflict in services.html using your code editor.

.Stages and commits the resolved merge conflict. git add services.html git commit -m "Resolve merge conflict between main and ft/service-redesign"

git push : Pushes the updated branch with the conflict resolution back to GitHub.

END OF THE SECOND BUNDLE


***************************************************************************************************************************************

