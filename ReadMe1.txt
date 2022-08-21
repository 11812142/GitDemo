Step 1 [Setup machine with git configuration]

1.Get version:>
git version
2.To configure 
git config --global user.name "username"
git config --global user.name "abc@gmail.com"
3. Check config
git config --global --list
-----------------------------------------------------

Step 2 [Integrate notepad++.exe to git & make default editor]

1. To check -->notepad++.exe execute from git bash
notepad++
if not then add path in environment variable
(Control panel-->System Advance system settings--> go to advance tab--> Environmentvariables -->add path)
2. open from git bash shell
now execute notepad++ command
3. To create an alias command 
notepad++.exe bash -profile
add this in notepad-> alias npp='notepad++.exe -multiInst -nosession'
4. To configure the editor 
git config --global core.editor "notepad++.exe -multiInst -nosession"
5. To verify if notepad++ is the default editor
git config --global -e
  output
   [user]
	name = abc@gmail.com
	email = abc@gmail.com
   [safe]
	directory = C:/Users/Pratibha Sheoran
   [core]
	editor = notepad++.exe -multiInst -nosession
------------------------------------------------------------

STEP 3 [add a file to source code repository]

1. In bash shell create a new project "GitDemo"
git init GitDemo
2. git bash iniitialize the "GitDemo"repo --> To verify
ls -al
3. create a file "welcome.txt" & add content
echo "Welcome to the version control" >> welcome.txt
4. To verify "welcome.txt"
ls -al
5. To verify the content
cat welcome.txt
6. Check the status
git status
7. To make the file to be tracked by git repo
git add welcome.txt
8. To add multi line comments,open default editor to comment
git commit
9. To check if local & "Working Directory" git repository are same -->check status
git status
10. SignUp in Gitlab & create a remote repository "GitDemo"
11. To pull the remote repository
git pull origin master
12. To push the local to remote repository
git push origin master



Git global setup
git config --global user.name "Pratibha Sheoran"
git config --global user.email "pratibhasheoran2000@gmail.com"
Create a new repository
git clone https://gitlab.com/pra-eoran/demo.git
cd demo
git switch -c main
touch README.md
git add README.md
git commit -m "add README"
git push -u origin main
Push an existing folder
cd existing_folder
git init --initial-branch=main
git remote add origin https://gitlab.com/pra-eoran/demo.git
git add .
git commit -m "Initial commit"
git push -u origin main
Push an existing Git repository
cd existing_repo
git remote rename origin old-origin
git remote add origin https://gitlab.com/pra-eoran/demo.git
git push -u origin --all
git push -u origin --tags