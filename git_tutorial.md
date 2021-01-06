# GIT Cheat Sheet

## Version Control System

`-` is a system that allows you to revisit various versions of a file or set of files by recording changes. Through version control, one can revert a file or project to a previous version, track modifications and modifying individuals, and compare changes. 

## What Is Git?

`-` Git is a free, open-source distributed version control system. It keeps track of projects and files as they change over time with the help of different contributors.

- Each time you save a changed version of your project — called commit — Git creates a snapshot of the file and stores a reference to it.
- Every single change applied to any file or directory is tracked by Git. And, as the gatekeeper, Git will always detect file corruption or loss of information in transit.
- Git is set up to greatly minimize the possibility of irreversible damage to files, such as accidentally lost data. Git makes it extremely difficult for a snapshot of your file that is committed to be lost.

## Some Of The Git Commands

1. **Cloning**
    - git clone https://github.com/test
    - copy of an existing Git repository from a particular server by using the clone command with a repository’s URL. By cloning the file, you have copied all versions of all files for a project.

2. **Check file status**
    - git status
    - we can determine the state of files.

3. **Creating a new file**
    - touch new_file.md
    - creates a local file in your computer

4. **Tracking and Staging a New File**
    - git add new_file.md _/Track one file only by using the following format/_
    - git add . _/Track all files in a repository/_
    - After using these commands, files are tracked and staged for committing

5. **Committing a File**
    - git commit -m “Your comment goes here”
    - After staging one or multiple files, you should commit the changes and record what you did within the commit message

6. **Committing All Changes**
    - git commit -a
    - This command commits a snapshot of all modifications to tracked files in the working directory.

7. **Pushing Changes**
    - git push origin main
    - This command pushes changes from the local “master” branch to the remote repository named “origin”.  

  
[<== Back to ReadMe](README.md)
    