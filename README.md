# Basics Of Git and Github

## Configuration

1. Name: git config --global user.name [username]

2. Email: git config --global user.email [email]

3. Default Editor: it config --global core.editor "code --wait"

4. Necessary config: git config --global core.autocrlf input  // 'true' instead of 'input' for windows

## General Commands 

1. Initialize a local directory to git repo: git init

2. Checking Status of changed files: git status

3. Adding files to staging: git add file1 file2   // or use '.' to add all the everything present

4. Commiting files to repo: git commit -m "Title of the changes made " -m "Desc of the changes made"

## Staging Specific Commands 

1. List files in staging: git ls-files

2. Remove or Move files/folders from staging + local directory: git rm/mv filename/foldername

3. Remove files/folders from staging only: git rm --cached file/foldername

## 