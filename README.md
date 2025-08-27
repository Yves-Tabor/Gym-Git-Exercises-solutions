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
