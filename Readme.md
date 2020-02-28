# Setting-Up-Git-Account
#### Basics that you need to get started with GIT

Setting the GIT account and syncing remote repository to github is sometimes tricky.Follow the steps for setting the remote GIT repository and GIT account.


# 1. Generate SSH key from remote server and add it to GITHUB SSH KEYs.
(Don't use '$' sign in the beginning as in do not copy it to the terminal)

--Setting up the user-name and user-email, it can be set to anything depending upon which name you want to show on your commits!                                                    
```$ git config --global user.name "username"```                                                            <br />
```$ git config --global user.email "user-email-address"```                                                 <br />

#### Note that the above user.name and user.email has nothing to with the credentials, you can have any user.name that you want to show on the commit message! A global user.name can be used or a repo user.name can be used after switching to that repo. <br />                                                                                                      <br />

--Remove the previous origin if present                                                                 <br />
```$ git remote rm origin```                                                                                <br />

--Add the git repo url as origin                                                              </br>
```$ git remote add origin SSH-url-of-GIT-repo```                                                           <br />


--Generating the SSH key for adding it to the GIT account                                               <br />
```$ cd ~/.ssh```                                                                                           <br />
```$ ssh-keygen -t rsa -C "email_address"```                                                                                          <br />


--Opening the generated key for displaying it in the terminal. Copy the key and add it to the git account.       <br />
```$ cat ~/.ssh/id_rsa.pub```                      <br />
Add this key to your github account.         <br />


```$ ssh -T git@github.com```                                    <br />
You will get a welcome message in your console.            <br />


Now go your project folder and command:

```git push -u origin master```

now it works!     <br />


------------------------------------------------------------------------------------------------------------------------------


# 2. Steps to follow before pushing the files from the repository to GIT account. <br />


first of all go to the project folder and the initialize Git init command as:                               <br />

```$ git init```                                               <br />

```$ git remote add origin SSH-url-of-GIT-repo```              <br />

(Do not forget to add all the files and commit the changes before pushing the files to GIT account)         <br />

```$ git add .```                                              <br />
```$ git commit -m "initial commit"```                         <br />
```$ git push origin master```                                 <br />





------------------------------------------------------------------------------------------------------------------------------

# Useful Git commads:

</br>

```$ git add .``` </br>
It adds all the changes that you have made on the working repository to the staging area.
</br>
</br>

```$ git commit -m “initial commit”```</br>
It commits all the changes to the staging area to the remote repository.
</br>


</br>

```$ git log```</br>
Use this command to see all the commit history.
</br>
</br>

```$ git status```</br>
Use this command to see all the modifications done to the staging area and working repository.
</br>

</br>

```$ git diff```</br>
Use this command to see the differences between the working reposiroty and the staging area.
</br>

</br>

```$ git diff --staged```</br>
Use this command to view the difference between the staging area and the remote repository.
</br>

</br>

>`HEAD`: HEAD is actually your current commit, or you can say it is your latest commit.</br>
`Origin`: The remote repository is known as origin, which is present on the GitHub account.

</br>

```$ git reset --hard commit_id``` </br>
```$ git push --force``` </br>
It will undo the changes till the commit_id provided in the above command. commit_id can be found using the git log command.

</br>

```$ git reset --hard HEAD```</br>
It will remove all the tracked and the untracked changes, it means it will remove all the work done that is saved to the staging area ($ git add .) or not saved to the staging area until the latest commit. The removed data can-not be brought back.
</br>

</br>

```$ git reset --hard origin/master```</br>
It will remove all the uncommitted changes from the current branch and will make it same as remote repository.
</br>

</br>

```$ git push origin master```</br>
Meaning: It means to push all local changes from master to your remote repository origin.
</br>

</br>

```$ git push origin master:my_data_branc```h</br>
It means that you are pushing changes from your local master to remote origin, but it is renamed to origin/my_data_branch.
</br>

</br>

```$ git branch new_branch```</br>
It means you are creating a new branch named as new_branch.
</br>

</br>

```$ git checkout new_branch```</br>
It means you are now moved to the new_branch.
</br>

</br>

```$ git checkout -b new_branch```</br>
It means that you have created a new branch new_branch and you have moved to the newly created branch new_branch.
</br>

</br>

```$ git merge new_branch master```</br>
Note: Before merging the two branches, use git checkout master and then use this command so that you stays on Master and the new_branch is merged to the master branch.
</br>

</br>

```$ git -d new_branch```</br>
Used for deleting a branch.</br>



</br>

```$ git rm --cached -f *.DS_Store```</br>
Used for removing .DS_Store folder from the remote repository as it was already present before adding the .gitignore to the remote repository.
</br>
</br>


`cd .ssh` </br>
Viewing the private key stored in Mac for SSH
</br>
</br>

`ssh-keygen -p -f ~/.ssh/id_rsa` </br>
ADDING or UPDATING a passphrase for the private key
>Use a passphrase for the private key to make it even more secure
</br>

`ssh-add -K ~/.ssh/id_rsa` </br>
Avoiding Terminal to ask for Passphrase for the private key(Adding identity to SSH agent)
</br>
</br>

`ls -al ~/.ssh` </br>
View all the SSH keys
</br>
 </br>

`~/.ssh/config ` </br>
View the SSH configuration file
</br>
</br>

`touch ~/.ssh/config` </br>
Creating a configuration file for SSH keys
</br>
</br>

`git config --list` </br>
View the Git configuration file
</br>
</br>

`git config credential.helper` </br>
Git's stored passwords
</br>
</br>

`git credential-cache exit` </br>
Clearing a git account saved credentials
</br>
