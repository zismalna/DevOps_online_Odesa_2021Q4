# Git
### Results of my work with git
Setting up git environment:
```sh
git config --global user.name "Mykhailo Lopaiev"
git config --global user.email zismalna@gmail.com
git config --global core.editor vim
```
Created a remote repository, then cloned it to my local machine:
```sh
git clone https://github.com/zismalna/DevOps_online_Odesa_2020Q42021Q1.git
```
Learned how to add files to the staging area:
```sh
git add readme.txt
```
and then commit them to the  local repository:
```sh
git commit -m "adding empty readme.txt"
```
Learned how to create and merge branches:
```sh
git branch develop
git branch images
git branch styles
```

```sh
git checkout develop
git merge images
git merge styles
```
Resolved merging conflict by editing the conflicting file and re-committing it to the develop branch.

Used *git log* and *reflog* to review the commit history and write it to the file.

Used *git push* to sync all my committed changes to my GitHub repository.

# DevOps

DevOps is a combination of practices and tools aimed at bridging the gap between the developers who write the code, and system engineers who deliver said code to the infrastructure. DevOps principles aim to streamline the process of testing and delivering the final product, increasing stability and reliablility of releases.