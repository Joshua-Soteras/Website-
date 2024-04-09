 # Git + Github
Date:  1/21/24 
Last Updated: 4/2/24

## Intro: The Difference between Git and Github
**Git**: a distributed version control systems i.e. a tool that allows a user to keep track of changes in their codebase. Used to collborate with others and manage different versions of their code <br>
**Github**: web based hosting service ofr Git repos. Provides devleopers to store their Git repos. 

## Setting up SSH Keys 
Overview: 
- Allows for ease of access; no need to enter creditials every single time
- Secure Communication
- auth: access to repo / sign: signing commits
- in order to push, you need to prove that you are the owner of the account; SSH keys allow this 
  
0. About SSH
  - https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh 

1. Check for existing SSH key
- https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys
- ~/.ssh/id_ed25519.pub 

2. Generate a new SSH key
  - Source: https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

3. Adding a new SSH key tp 
  - Source : https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account

4. About commit Signature Verifivation
- https://docs.github.com/en/authentication/managing-commit-signature-verification/about-commit-signature-verification

5. mananging remote repo
- https://docs.github.com/en/get-started/getting-started-with-git/managing-remote-repositories#switching-remote-urls-from-https-to-ssh
- helps understanding changing from remote destination (from local to remote "address")
6. Testing SSH connection
  - source: https://docs.github.com/en/authentication/connecting-to-github-with-ssh/testing-your-ssh-connection 

## Commands 
_**git status**_<br> 
Can Verify the following: 
- if the local repo has been initialized

_**git remote**_ <br>
- The ```git remote -v```command is used in Git to view the remote repositories associated with your local repository. It displays the URLs of the remote repositories along with their corresponding fetch and push URLs
``` git remote -v``` 

## Working with Git + Github
### Setting Up Local Repo 
- ``` git init```
   - used to initialize a new Git Repository in an existing directory
   - sets up the necessarry data structures and files in the current dir. (folder) where it stores metadata and history to allow version control.

- ```git clone "url"```
  - when using this command in whichever directory (folder) you are going to clone locally, the directory will be initialized by default
  - clones the remote repo into the designated local repo 

### Managing Remote Repositories  
- ``` git remote rm nameOfDestination```
   - takes one argument: nameOfDestination (use git remote -v to see list) 


### Linking from Local to Remote
- ```git remote add```
  - takes two arguments: a remote name; example is _origin_
  - a remote URL
  - example : ```git remote add origin https://github.com/OWNER/REPOSITORY.git```
- ```git remote -v```
  - list the exisiting remote repos
  - can verify if URL remote has changed 
- ```git remote set-url origin https....insertURLhere```
  - change your remote's URL from SSH to HTTPS
    
### Pushing your work to a Remote Repository (GitHub) 
``` git add \\insert name of file ```
- stage your files and changes for a _commit_
- track your files and changes
- If you created a new file within the repo, then Git to track this file to commit
-	note: use '.'  to add all files / otherwise, you can just state the individual files
  - git add . #all files and folders
  -  git add index.html #individual files

``` git commit -m \\insert message here```



https://code.visualstudio.com/docs/sourcecontrol/overview
