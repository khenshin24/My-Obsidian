Create a repository

	create an app then publish
		then authorize git ecosystem 



https://www.youtube.com/watch?v=LcuzlEv8qRI&t=730s


"develop branch"
merge develop to other branch
commit all changes first
git fetch --all           // to fetch all branches
git merge origin/your-branch




currently
developing branch then need to move to other branch new 
create branch then push,




make sure you are in the correct directory!
![[Pasted image 20230517133655.png]]

create new branch
after creating new branch
```git push --set-upstream origin branchName
   git pull origin develop ```




case 
 back to oginal branch
 example if you pull other branch in your branch then you merge it and commit it
 but now you want to back the branch to original because you encountered lot of conflicts
 use this code
 git reflog
 then copy the reference code
 example
 
 ```
```
	abcd123 HEAD@{0}: pull origin IKON-560: Merge made
	1234abc HEAD@{1}: checkout: moving from some-branch to IKON-608
```

then 

	git reset --hard 1234abc

