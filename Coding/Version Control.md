---
sticker: lucide//github
---
- Commit often and write good comments. 
- Commit changes related to only one feature or task of a program. 

**Local Git**
```bash
git init   # start VC in local directory

git status # shows files (tracked and untracked)

git add {file.name} # adds file to staging area to track changes
	add . # adds everything in the directory

git commit -m "message" # add file to VC, write in Present Tense. 

git log # shows commits made

git diff {file.name} # look at the differences between two files 

git checkout {file.name} # to revert back to previous version. 

git rebase # Reorganises commit history. 
```

**GitHub**
```bash
git remote add origin {link} # Create a remote repository

git push -u origin main #Push local repo to remote one on main btranch 
```

**Git ignore**
```bash
touch .gitignore #add file names to be ignored, can find useful ones on GitHub
```

**Git Clone**
- Awesome for beginners on GitHub
```bash
git clone {link} #allows to build on existing code. Open source contributions
```

**Branching and merging**
- Create different branches to test out new features or ideas. 
- Can then merge branches into main to bring in changes once everything works. 
```bash
git branch {name} #use without name to check the branches
git checkout {branch} #move to different branch
git merge {name of branch}
```

**Forking and Pull requests**
- Copy remote repo, pull request needs to be made to add updates to OG repo. 

**Merge Issues**
- Building on same part of the code. 
- Branch being too old - spending too much time on a brach. 
- Make only one person responsible for mainline to avoid just pushing at random. 

Conventions are dictated by company policy. 

**Github Issues**
Create new issues that need to be worked on - Bugs, feature requests and TODOs 


*Other*
Track progress using a readme file. 


**GitHub Actions**


**Best Practices**
- Branching strategy - how SC is managed
	- Main - working version of your code. 
	- Always create a branch from main when making changes. 
	- Feature branches - Used to work on specific features. 
	- Release branches - Stabilise code before release. 
	- Hot Fix - Critical issue fix. 
- Commit message conventions
	- Keep lines concise
	- Reference requests
- Code review etiquette
	- Constructive feedback. 
	- Timely reviews - keep it moving. 
- Issue and project management
	- Issues to track tasks, bugs. 
	- Use Projects section for management. 
- Security considerations
	- Dependency scanning 
	- Code analysis 
	- Access control. 