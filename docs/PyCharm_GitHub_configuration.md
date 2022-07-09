## Step By Step Process for creating the Pycharm Project and Linked with Github

### Create new repo in Github:
1. First sign-in in GitHub with the account
2. Create "New repository" (*select README.md, .gitignore, license*)
3. create new branch "dev-01" from "master"


### Create new Project in Pycharm:
1. open Pycharm, select "new Project" to create new project:
	1. select specified folder for location
	2. select "New environment using"
		1. location will be, above specified folder/env
		2. choose "Inherit global site-packages"
	3. then select "create"
	
### Configure pycharm with github:
1. Once project created, go to "VCS"
2. then "create git repository" (select the repo folder)
3. Now "Git" menu will be visible and go to "Git"
	1. Then click on "Manage Remotes"
	2. keep remote name as "origin"
	3. provide the git https link as url.
4. go to "git" -> "GitHub" -> "create pull request"
	1. base fork: easycloudapi:cloudapi
	2. base branch: dev-01
	3. title: dev-01
5. if still pull request has been failed, 
	1. then go to right below, click on "master" branch and change to remote branches "origin/dev-01"
	2. click first "checkout"
	3. then click, "Pull into current using merge"