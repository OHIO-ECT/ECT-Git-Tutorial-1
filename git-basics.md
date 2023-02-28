# ECT Git Tutorial 1

### Git with a simple local repo

1. Make a new "project directory". Use good "file hygiene", Don't throw everything in the user home directory or "My Documents". The Linux "mkdir" command is responsible for making directories in the shell environment.
    ````
    mkdir ~/ect-git-tutorial-1
    ````
2. Change the current working directory to this project to simplify future commands.
    ````
    cd ~/ect-git-tutorial-1
    ````
3. Run the following command to show the contents of the working directory. In most unix shells files and directories that start with a . are considered "hidden". The -al flags to the ls application instruct that application to show the hidden directories and additional details.
    ````
    ls -al
    ````
4. Run the following command to create (initialize -- init) an empty git repository. The current directory will forever be known as the "working tree" or "working directory" for this git project.
    ````
    git init
    ````
5. Run the following command to show the contents of the current directory. Notice that the directory is not empty now, and .git directory contains the "index" for the git project.
    ````
    ls -al
    ````
6. **[Data]** The .git directory is the un the following command to show all of the file that exist under the current working directory including the files that make use the git index. 

    **[WARNING]** Editing the files in the git index directory is very hazardous to the  stability of the repositiory, and work can be lost.
    ````
    find .
    ````
7. **[Pro Tip]** To change the default editor to Nano. Just in case VIM isn't to your liking.
    ````
    git config --global core.editor "nano"
    ````
8. Use your favorite editor to create a file in the project directory. **Yes please use this file name, it will matter later.**
    ````
    nano README.md
    ````
9. Documentation is critical to any IT systems, networks, software, etc. Add some text to this file that will help future readers understand what this project is for. Save the document and return to the command line.

10. Make git aware of this new file by "adding" it to the git index.
    ````
    git add README.md
    ````
11. Commit this addition to the git repo with the commit command. Note the error message and move on to the next instruction.
    ````
    git commit -m "Test Comment"
    ````
12. Git often has helpful commands that the software recommends running next. On accounts that have not used Git before, the system requires editing the git configuration to include the users name and email address. Follow the instructions configure the user information.

13. Re-run the git commit command. Git demands a comment to be included in the commit in the form an nano editor window. Add some simple text describing the action being taken, write the file and exit the editor to complete the commit.

14. Edit the README.md and add an additional text.

15. There are now two copies of the README.md file on the local system. One in the working tree which is visible to the user and one in the index which is not. It is important to keep these two file insync with each other. The following git command will show the status of the two copies.
    ````
    git status
    ````
16. Repeat the git add README.md and then git commit commands sequence.

17. Run the following command to show more information about the status of the repository including information on the last change made.
    ````
    git status
    ````