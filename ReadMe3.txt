BRANCHING & MERGING

git clone "url"
cd repository
git status
git branch (create branch)
git branch branch_name
git checkout  branch_name
git branch (its shows * before branch)
[to check what dir in master]-->git checkout master-->dir-->cat file_name

To Check existing commd master 
git log --oneline --decorate  --graph

[to change in dir in branch_name]--git checkout master-->dir-->cat file_name

To Check existing commd branch 
git log --oneline --decorate  --graph
[NOTE: When a new branch is created, the complete commit history of the master branch is replicated]

--> {to made changes open}--> notepad file_name {made changes & check -->cat file_name}


Now check status-->git status
git add. ---> git commit -m 'Task done'
{this is all about local changes}

to chnge remotely
--> git push origin Branch_name

//{same in master}
//git checkout master-->dir-->cat file_name


[git GUI --{to view diffences pictorially}]
C/program_files/git/source/rightclick-opn Git GUI-->repository-->visuallize all branch history

[git diff]
git diff master..branch_name

Lets Merging 
{Note: You need to be in repository where u want to merge}
git merge branch_name

[git diff commad to see changes and u will not see any change]
git diff master..branch_name
git log --oneline --decorate  --graph
{updated in gui}

to delete branch
git branch -d branch_name










