# Basics Of Git and Github

## Configuration

1. Name: git config --global user.name [username]

2. Email: git config --global user.email [email]

3. Default Editor: it config --global core.editor "code --wait"

4. Necessary config: git config --global core.autocrlf input  // 'true' instead of 'input' for windows

5. Difftool config: git config --global diff.tool vscode

                    git config --global difftool.vscode.cmd "code --wait $LOCALHOST $REMOTE"
 

## General Commands 

1. Initialize a local directory to git repo: git init

2. Checking Status of changed files: git status  // use '-s' parameter for less info

3. Adding files to staging: git add file1 file2   // or use '.' to add all the everything present

4. Commiting files to repo: git commit -m "Title of the changes made " -m "Desc of the changes made"

5. See changes made to files of: 
        Last staging: git difftool
        Last commit: git difftool --staged

6. Restoring files to last staging version in the local directory: git restore [filename]
   Restoring to a specific version: git restore --source=HEAD~n [filename ]




## Staging Specific Commands 

1. List files in staging: git ls-files

2. Remove or Move files/folders from staging + local directory: git rm/mv [filename/foldername]

3. Remove files/folders from staging only: git rm --cached [file/foldername]

4. Unstaging: git restore --staged [filename]
   The file will be restored to the last commit version in the staging 
## Ignoring Files/Folders to prevent from commiting (eg: executable or log files)

1. Create a file: .gitignore

2. Add name of files/folders to be ignored 

3. NOTE: THE FILES/FOLDERS ALREADY COMMITED CAN'T BE IGNORED LATER

( www.github.com/github/gitignore : to find templates of files to be ignored for different languages )

## Viewing Commit Log:

1. Showing info of all Commits : git log --oneline

2. Show the changes made in Head minus nth commit (head is the latest commit): git show HEAD~n // if need to show the latest commit then just use 'HEAD'

3. To show final version of the file in Head minus nth commit: git show HEAD~n: [filename]

4. To show all files/folders affected by a commit statement: git ls-tree HEAD~n

5. To see the final version of a file/folder with its uniqueId: git show [uniqueId] 

