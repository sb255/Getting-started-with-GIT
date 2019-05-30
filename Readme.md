# SB255-Setting-Up-Git-Account
Basics that you need to get started with GIT

Setting the GIT account and syncing remote repository to github is sometimes tricky.Follow the steps for setting the remote GIT repository and GIT account. 


# 1. Generate SSH key from remote server and add it to GITHUB SSH KEYs.
(Don't use '$' sign in the beginning as in do not copy it to the terminal)


```$ git config --global user.name "username"```                                                            <br />
```$ git config --global user.email "user-email-address"```                                                 <br />
                                                                                                      <br />

--Remove the previous origin if present                                                                 <br />
```$ git remote rm origin```                                                                                <br />

--Add the git repo url as origin                                                              </br>
```$ git remote add origin SSH-url-of-GIT-repo```                                                           <br />
  

--Generating the SSH key for adding it to the GIT account                                               <br />
```$ cd ~/.ssh```                                                                                           <br />
```$ ssh-keygen```                                                                                          <br />


--Opening the generated key for displaying it in the terminal. Copy the key and add it to the git account.       <br />
```$ cat ~/.ssh/id_rsa.pub```                      <br />
Add this key to your github account.         <br />


```$ ssh -T git@github.com```                                    <br />
You will get a welcome message in your console.            <br />


Now go your project folder. git push -u origin master, now it works!     <br />


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
