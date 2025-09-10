## Lab 03

- Name: Jaeden A Rodriguez
- Email: rodriguez.192@wright.edu

## Part 1 - git Guide

| git command         | Description |
| ---                 | ---         | 
| `git clone repo_URI`|   Git clone creates a local copy of a remote repository on your computer, allowing you to work locally and push changes back onto the original repository.          |
| `git status`        |  The git status command is used to display the state of the working directory and the staging area.            |
| `git add filename`  |     This git add filename command adds new or changed files to your working directory, which marks it for inclusion during the next commit.        |
| `git commit`        |       Git commit is fundamental command that captures a record or "snapshot" of changes since the last commit changes, acting like a "save point" at that given time.      |
| `git push`          |      Git push allows you to upload and transfer files, content, or changes from your local respository to a remote respoitory,.      |
| `git pull`          |   Git pull is used to incorporate and integrate changes from a remote repository into your local branch, effectively matching the contents between the workspace and repository the same.    |

## Part 2 - clone

1. Command to generate an SSH key with ed25519: ssh-keygen -t ed25519 -C rodriguez.192@wright.edu
2. Command(s) to read & copy text of the *public* key: cat ~/.ssh/id_ed25519.pub
3. Summary of steps to place *public* key in user profile: Copy public key (Step 2), Go to Github --> Settings --> SSH Keys and GPG Keys, Click New SSH Key, Give it a Title, Paste SSH Key in Field, then Save
4. Command to *clone* your `ceg2350s25-YOURGITHUBUSERNAME` with SSH for authentication: git clone @github.com:ceg2350s25-JaequazaTube/ceg2350s25-JaequazaTube.git

## Part 3 - IO Redirection

1. `printenv HOME > thishouse`
   - Explanation: Writes the path to the home directory into a file called "thishouse" by printing environmental variables through printenv.
2. `cat doesnotexist 2>> hush.txt`
   - Explanation: The "cat" command tries to read and display doesnotexist, but results in an error. That error message is then appended to hush.txt for later use.
3. `cat nums.txt | sort -n >> all_nums.txt`
   - Explanation: "Cat" reads the contents of nums.txt and sorts them in numeric order (treating them like numbers thanks to that -n), and then sends the finished sorted result to all_nums.txt.
4. `cat << "DONE" > here.txt`
   - Explanation: This command will wait for lines of text to be typed by you (the user), and will continue adding whatever you type into here.txt until it sees DONE on a separate line.
5. `ls -lt ~ | head`
   - Explanation: Ls "lists", and "-lt" organizes the retrieved files by length and time, essentially showing your most recently modified files in your home directory in a set of 10.
6. `history | grep ".md"`
   - Explanation: Will showcase the history through grep, which searches for text patterns, of all file entries marked with the .md personifier at the end. 

## Part 4 - Rolling the Dice

Verify that `roll` made it to your GitHub repository for this course and is in your `Lab03` folder.  No answers will be written here unless you would like to leave a note to the TAs

## Part 5 - Retrospective Answers

1. Where and when did it go wrong while working on your script tasks?
> Your reflection here
2. Was anything familiar working with a new language compared to one you are used to?
> Your reflection here
3. Did you write good `commit` messages that refer to what tasks were completed at each commit?  What would you improve?
> Your reflection here

## Extra Credit

1. Note here *what* you did to the script for the extra credit.

## Citations

To add citations, provide the site and a summary of what it assisted you with.  If generative AI was used, include which generative AI system was used and what prompt(s) you fed it.  Generative AI may not write your script for you, only assist with component and how to type questions.
