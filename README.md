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
	
	git checkout -b homepage
	
	git branch (Should print 'homepage')





