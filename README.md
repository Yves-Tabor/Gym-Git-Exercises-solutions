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

BUNDLE THREE
 
Yves-Tabor edited this page last week · 3 revisions
# Exercise 1 :
Question :

Create a new branch named ft/team-page
Create a new html page named team.html and add some changes
commit and push those changes
Create a new PR for the changes
Go back to main branch (checkout the main branch)
Create new branch named ft/contact-page
Go back to the ft/team-page
With the help of git log look for the last commit and copy its hash
Checkout again ft/contact-page using git cherry-pick get the changes from the last commit on the ft/team-page branch.
Add new changes for the contact page and commit, push them
Create a new PR for the contact page
From the ft/contact-page branch create a new branch called ft/faq-page
Create a new faq.html page and add some changes there
Commit and push those changes
Using git revert, revert the changes of the last commit of the ft/team-page branch. (use the commit hash you copied earlier)
Push the changes and create a new PR
Git Process :

git checkout -b ft/team-page :Creates and switches to a new branch named ft/team-page.

echo "

<title>Team</title>
Our Team
" > team.html : Creates a new HTML file team.html with basic content.
git add team.html git commit -m "Add team.html page"

git push -u origin ft/team-page : Pushes the ft/team-page branch to the remote and sets it as upstream.

. Go to GitHub and create a Pull Request (PR) from ft/team-page into main.

git checkout main : Switches back to the main branch.

git checkout -b ft/contact-page : Creates and switches to a new branch named ft/contact-page.

git checkout ft/team-page : Switches back to the ft/team-page branch.

git log --oneline : Displays a concise list of recent commits. Copy the hash of the last commit (the one for team.html).

git checkout ft/contact-page : Switches back to the ft/contact-page branch.

git cherry-pick : Applies the changes from the last commit in ft/team-page to ft/contact-page. Replace <commit-hash> with the copied hash.

echo "

<title>Contact</title>
Contact Us
" > contact.html : Creates a new HTML file contact.html with basic content.
git add . git commit -m "Add contact.html page"

git push -u origin ft/contact-page : Pushes the ft/contact-page branch to the remote.

.Go to GitHub and create a PR from ft/contact-page into main.

git checkout -b ft/faq-page : Creates and switches to a new branch from ft/contact-page named ft/faq-page.

echo "

<title>FAQ</title>
Frequently Asked Questions
" > faq.html : Creates a new HTML file faq.html with basic content.
git add faq.html git commit -m "Add faq.html page"

git push -u origin ft/faq-page : Pushes the ft/faq-page branch to the remote.

git checkout ft/team-page : Switches back to the ft/team-page branch.

git revert : Reverts the changes of the last commit (used earlier for cherry-pick). Replace <commit-hash> with the actual commit hash.

git push : Pushes the revert commit to the remote repository.

.Go to GitHub and create a PR for the revert commit in ft/team-page.

# Exercise 2 :
Question :

Create new branch from the ft/faq-page branch named ft/home-page-redesign
Go back to the main branch and make some changes there
Commit and push them
go back to the ft/home-page-redesign branch
Using git rebase, rebase your branch to main
Add changes to the home page and commit push them
Create a PR for the changes.
Git Process :

git checkout ft/faq-page : Switches to the ft/faq-page branch.

git checkout -b ft/home-page-redesign : Creates a new branch ft/home-page-redesign from ft/faq-page.

git checkout main : Switches back to the main branch.

echo "

New section added to the main branch homepage.

" >> index.html : Simulates a change on the main branch (e.g. homepage update).
git add index.html git commit -m "Update homepage on main branch"

git push origin main : Pushes the latest commit to the remote main branch.

git checkout ft/home-page-redesign : Switches back to the ft/home-page-redesign branch.

git rebase main : Rebases the ft/home-page-redesign branch onto the latest main changes (linear history).

echo "

Redesigned Home Section
" >> index.html : Adds new homepage redesign content.
git add index.html git commit -m "Redesign home page section" : Stages and commits the redesign changes.

git push -u origin ft/home-page-redesign : Pushes the rebased branch to the remote.

Now go to GitHub and create a Pull Request from ft/home-page-redesign into main.

END OF THE THIRD BUNDLE

****************************************************************************************************************************************

BUNDLE FOUR
 
Yves-Tabor edited this page last week · 2 revisions
# Exercise 1 :
Question :

Checkout the main branch
Create a new repository on Github
Using git remote add the repo to your project as second remote named git-copy
Make a new changes on the home page
Commit the changes
Push the changes to the both remotes. the origin and git-copy
Git Process :

git checkout main : Switches to the main branch of your project.

. Go to GitHub and create a new repository (leave it empty — no README, license, or .gitignore).

git remote add git-copy https://github.com/your-username/your-second-repo.git : Adds the newly

.created GitHub repo as a second remote named git-copy.

echo "

© 2025 Company

" >> index.html : Makes a change to the homepage by adding a footer to index.html.
git add index.html git commit -m "Add footer to homepage"

git push origin main : Pushes the commit to the original remote repository (origin).

git push git-copy main : Pushes the same commit to the second remote (git-copy).

# Exercise 2 :
Question :

Checkout a new branch named ft/footer
Add some changes to the branch and commit them
Add more changes again to the branch and create a second commit
Push and create a new PR for the branch
Checkout the main branch again
From there create a new branch named ft/squashing
Using git merge squash, squash the changes on the ft/footer branch
Commit the changes with a different commit message such as footer changes squashing
Push the changes and create a PR
Git Process :

git checkout -b ft/footer : Creates and switches to a new branch named ft/footer.

echo "

Initial footer content

" >> index.html : Adds initial footer content to the homepage.
git add index.html git commit -m "Add initial footer section"

echo "

Updated footer with contact info

" >> index.html : Adds more content to the same footer section.
git add index.html git commit -m "Update footer with contact info"

git push -u origin ft/footer : Pushes the ft/footer branch to the remote.

.Now go to GitHub and create a Pull Request from ft/footer into main.

git checkout main : witches back to the main branch.

git checkout -b ft/squashing : Creates and switches to a new branch named ft/squashing from main.

git merge --squash ft/footer : Merges the ft/footer branch into ft/squashing but combines all commits into one.

git commit -m "footer changes squashing" : Commits the squashed changes with a custom message.

git push -u origin ft/squashing : Pushes the new branch to the remote.

.Now go to GitHub and create a PR from ft/squashing into main.

END OF FOURTH BUNDLE

****************************************************************************************************************************************

BUNDLE FIVE
 
Yves-Tabor edited this page last week · 1 revision
# Exercise 1 :
Question :

On your Github repo enable Github pages
Check if the link is publicly visible to anyone
Git Process :

Let's go to the GitHub repository in your web browser. Open the repository where you want to enable GitHub Pages.

Click on the "Settings" tab. Opens the repository settings.

In the left sidebar, scroll down and click "Pages" (under "Code and automation" or “Pages”). Navigates to the GitHub Pages configuration.

Under "Source", select the branch (e.g. main) and folder (/root if your files are in the main folder). This sets the source for GitHub Pages deployment.

Click "Save". Applies your GitHub Pages configuration.

After saving, GitHub will provide you with a public URL — something like: https://your-username.github.io/your-repo-name/

This is your live GitHub Pages site link.

Open the link in an incognito/private browser window or log out of GitHub and try the link. This ensures that the page is publicly visible and not restricted to your GitHub account.
If the page loads successfully without requiring a login, then your GitHub Pages site is publicly visible.

# Exercise 2 :
Question :

Fork this project https://github.com/TheGymRwanda/git-cafe-exercise
Clone your fork on your machine
Edit the index.html file
Change the text Welcome to our place to Welcome to our restaurant
Commit and push the changes
Raise a PR to the original Repo
Git Process :

For example go to https://github.com/TheGymRwanda/git-cafe-exercise and click “Fork" (top-right corner). This creates a copy of the repository under your GitHub account.

Copy the clone URL from your fork (e.g. https://github.com/your-username/git-cafe-exercise.git). This is used to clone your forked repo to your machine.

Run this in your terminal: git clone https://github.com/your-username/git-cafe-exercise.git Clones your forked repository locally (replace with your actual fork URL).

cd git-cafe-exercise Navigates into the project folder.

Open the file index.html in your code editor. Prepares to make your required text change.

Find the text Welcome to our place and change it to Welcome to our restaurant. Updates the greeting message as instructed.

Save the file and return to your terminal: git add index.html Stages the updated file.

git commit -m "Update welcome text to 'Welcome to our restaurant'" Commits the change with a descriptive message.

git push origin main Pushes your change to your forked GitHub repository.

Go to your forked repo on GitHub, and click “Contribute” > “Open pull request”. Starts the process to raise a PR to the original repo.

Review the PR, then click “Create pull request”. Submits your pull request to the original repository for review.

END OF THE FIFTH BUNDLE

*****************************************************************************************************************************************
