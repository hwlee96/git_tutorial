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