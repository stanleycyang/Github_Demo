#Team Git Practices


##Lesson Objectives

- Explain what branching is, why you would branch, and how to branch.
- Be able to branch, merge, and resolve conflicts when working in a team.


##Branching Commands

	git branch - This lists your available branches.

	git branch branchname - This creates a new branch.
	
	git branch -v  - To see the last commit on each branch.
	
	git checkout -b branchname - This creates and immediately switchs to a branch.
	git checkout branchname - Switches you to another branch.
	
	git branch -d branchname - This deletes a branch.
	
	git merge branchname - This merges a branch onto the branch you're sitting on (If you're on the master branch, it mersges branchname into master).


##Quick Demo


Create an app
	
	rails new Github_demo
	rails s -p 4000
	rails g controller StaticPages home about

Change routes

	# routes.rb	
	
	root 'static_pages#home'
    get 'about' => 'static_pages#about'
    
Grab a partner sitting next to you, one of you guys will create a repo and add the other as a collaborator!

	1. Go into Github repo
	2. Click Settings
	3. Click Collaborators on your left hand corner
	4. Find your partner and add them as collaborator

Initialize Repo

	git init
	
	git remote add origin https://github.com/syang019/Github_Demo.git
	
	git push -u origin master
	
One of you will work on home page, the other will work on about page
	
	git checkout -b homepage / aboutpage
	
	git branch (Should print the name of branch)


Each of you will add a h1 title to your page (home.html.erb or about.html.erb) then add / commit the changes to your branch

	git add -A
	git commit -m "Changed (homepage/aboutpage) page"
	git push origin (homepage/aboutpage)

Then compare your branch against the master by typing the following:

	git branch -v

Then, go onto Github and create a pull request
	
	1. On GitHub, navigate to the repository from which you'd like to propose changes.
	
	2. Branch dropdown menuIn the "Branch" menu, choose the branch that contains your commits.
	
	3. Pull Request buttonTo the left of the "Branch" menu, click the green Compare and Review button.
	
	4. Edit button for compare pageThe Compare page will automatically select the base and compare branches; to change these, click Edit.
	
	5. Create pull request buttonOn the Compare page, click Create pull request.
	
	6. Pull Request description pageType a title and description for your pull request.
	
	7. Send Pull Request buttonClick Create pull request.

**Source:**
	
[Creating a pull request in Github](https://help.github.com/articles/creating-a-pull-request)

View the pull request and merge it with master

	git checkout master
	git pull

If you are done with the homepage / aboutpage feature, delete the branch

	git branch -d homepage / aboutpage

Or, if you were to continue, you can merge master with your branch

	git merge master (from your feature branch)
	
If you have merge conflicts, subl . or git mergetool to resolve conflicts

To configure your mergetool, use

	git config --global merge.tool kdiff3

**Resolving Merge Conflicts**

[Resolving Merge Conflicts](https://help.github.com/articles/resolving-merge-conflicts/)
	



