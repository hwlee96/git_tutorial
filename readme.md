###Setting up a new repo repo
###Setting up a new

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
