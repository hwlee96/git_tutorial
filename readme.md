###Setting up a new repo

1. Create new repo in github account first (havent found automatic method yet)
		a. Need to understand how github servers work first
2. In command line:
	```git init```
	```git add <files>```
	```git commit -m "first commit"```
	```git remote add origin git@github.com:hwlee96/<reponame>.git```
	```git push -u origin master```

### Resetting commits/adds

```git add .```
```git reset .```
* If you use ```git reset --hard``` , you will unstage the files and delete them forever
	
```git commit -m "Something terribly misguided"```     
```git reset HEAD~```                                    
<< edit files as necessary >>                              
```git add ...```  


### Git Branching
To create (if you haven't already) and change to branch specified if you haven't done so:
``` git checkout -b <branch-name>``` 
To just checkout existing branch:
``` git checkout <branch-name>``` 

### Git Stash
You don't necessarily have to commit your files before switching to the master branch there's a another mechanism to save your work in progress if you're working on something that's half-finished or experimental.

You can use a command called ```git stash``` 

```git stash -u```

This will save all of your current changes without committing them and then revert back to a clean working directory then later at some point in the future when you want to get back to work. You can either pop or apply the changes in that stash to your current working directory.

```git stash pop```

So kind of just like it sounds you're stashing away your current changes to be used at some later point so stashing is just a handy thing to know and an alternative to committing your code if you're not quite ready to do so.

### Squashing
A lot of times on a feature branch you'll create a lot of different commits and these commits are kind of irrelevant to what's going on in the master branch, e.g. you can see here that our feature branch is three commits ahead of our master branch and it has a bunch of comments about adding useless emojis to the code. 
Instead of merging all of these commits into the master branch you can use the squash flag to squash them down into a single commit. When you do so, your merge this will keep the change history nice and concise on the master branch but still preserve all of the original commits on the feature branch itself. 

```git merge <branch-name> squash```

When you merge with the squash flag, it won't actually change the head commit on the master branch so you'll need to add an additional commit on your own that says something like merged in feature branch and that gives us a nice compact change history on the master