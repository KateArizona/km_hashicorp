# km_hashicorp
Repository for the HashiCorp sample

## What is the difference between fetch, push, and pull?

The commands perform these functions:

- `git fetch`: Gets changes from a remote repo into your tracking branch
- `git push`: Sends changes from a local branch to a remote repo
- `git pull`: Gets changes from a remote branch into your tracking branch and merges them into a local branch

Use these commands to share code with a remote repository. Think of it as "make the remote branch resemble my local branch". 

Both `git push` and `git pull` are used to download data from the identified remote repository. However, the two commands are not equivalent.

`git pull` gets changes from the remote branch to the tracking branch and merges those changes. 
 
`git push` gets changes from the current branch and pushes the changes to the remote branch. 

Your `git push` fails when the remote branch has diverged from your local branch. Typically, this occurs when not all the remote branch commits are in your local branch. To fix this, synchronize your local branch needs with the remote branch with `git fetch` and `git merge`.

`git fetch` takes the current branch and verifies there is a tracking branch. Next, it looks for changes in the remote branch and pulls them into the tracking branch. It does not change your local branch. To change the local branch, use `git merge origin/master`(for the "master" branch) to merge those changes.  

While `git pull` simply does a `git fetch` followed immediately by `git merge`, you may want to use `git fetch` followed by `git merge` to make sure you understand the changes you are merging into your branch before the merge happens.

![image](https://user-images.githubusercontent.com/69814618/111831151-303d2c80-88ac-11eb-95b8-c2fa62cb7efc.png)

