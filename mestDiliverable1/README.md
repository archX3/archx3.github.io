//this is me creating a new markdown file for my first baby repo

```
- use:	git init
```
  in a folder to create a repo in a folder
"octobox" directory now has an empty repository in /.git/. The repository is a hidden directory where Git operates.

OR
```
- use: git init directoryName/sunDirectoryName

- use:	git status
```
  to see the current state of the project
// master branch gets created when u initialise a repo


#1.4 Adding Changes
Good, it looks like our Git repository is working properly. Notice how Git says octocat.txt is "untracked"? That means Git sees that octocat.txt is a new file.

To tell Git to start tracking changes made to octocat.txt, we first need to add it to the staging area by using git add.


```
 - use: git add octocat.txt
 
 - $ git status
```
##### On branch master
#####
##### Initial commit
#####
##### Changes to be committed:
```html
 - use git rm --cached <file>
```
to unstage a file
#####	[]new file:   octocat.txt[]


#1.6 Committing
Notice how Git says changes to be committed? The files listed here are in the Staging Area, and they are not in our repository yet. We could add or remove files from the stage before we store them in the repository.

To store our staged changes we run the commit command with a message describing what we've changed. Let's do that now by typing:

```
- use: git commit -m "Add cute octocat story" //for all files being tracked
- use: git commit -am "Add cute octocat story" //for all files being tracked and those that are not being tracked. (untracked files are added to the staging area)

- use: git commit fileName -m "message to add to describe the commit" // for single files

- use: git commit fileName1 fileName2 -m "message to add to describe the commit" // for single files
```


#1.7 Adding All Changes
Great! You also can use wildcards if you want to add many files of the same type. Notice that I've added a bunch of .txt files into your directory below.

I put some in a directory named "octofamily" and some others ended up in the root of our "octobox" directory. Luckily, we can add all the new files using a wildcard with git add. Don't forget the quotes!

use:
```
- git add '*.txt'
```

#1.8 Committing All Changes
Okay, you've added all the text files to the staging area. Feel free to run git status to see what you're about to commit.

If it looks good, go ahead and run:
```
- use:	git commit -m 'Add all the octocat txt files'
```

#1.9 History
So we've made a few commits. Now let's browse them to see what we changed.

Fortunately for us, there's git log. Think of Git's log as a journal that remembers all the changes we've committed so far, in the order we committed them. Try running it now:
```
- use:	git log
```

#1.10 Remote Repositories
Great job! We've gone ahead and created a new empty GitHub repository for you to use with Try Git at  https://github.com/try-git/try_git.git. To push our local repo to the GitHub server we'll need to add a remote repository.

This command takes a remote name and a repository URL, which in your case is https://github.com/try-git/try_git.git.

Go ahead and run git remote add with the options below:
```
- use:	git remote add origin https://github.com/try-git/try_git.git
```

#1.11 Pushing Remotely

The push command tells Git where to put our commits when we're ready, and now we're ready. So let's push our local changes to our origin repo (on GitHub).

The name of our remote is origin and the default local branch name is master. The -u tells Git to remember the parameters, so that next time we can simply run git push and Git will know what to do. Go ahead and push it!
```
- git push -u origin master
```


#1.12 Pulling Remotely

Let's pretend some time has passed. We've invited other people to our GitHub project who have pulled your changes, made their own commits, and pushed them.

We can check for changes on our GitHub repository and pull down any new changes by running:
```
- git pull origin master
```

#1.13 Differences

Uh oh, looks like there have been some additions and changes to the octocat family. Let's take a look at what is different from our last commit by using the git diff command.

In this case we want the diff of our most recent commit, which we can refer to using the HEAD pointer.
```
- git diff HEAD
```


#1.14 Staged Differences

Another great use for diff is looking at changes within files that have already been staged. Remember, staged files are files we have told git that are ready to be committed.

Let's use git add to stage octofamily/octodog.txt, which I just added to the family for you.
```
- git add octofamily/octodog.txt
```

#1.15 Staged Differences (cont'd)

Good, now go ahead and run git diff with the --staged option to see the changes you just staged. You should see that octodog.txt was created.
``` terminal
- git diff --staged
``` 


#1.16 Resetting the Stage

So now that octodog is part of the family, octocat is all depressed. Since we love octocat more than octodog, we'll turn his frown around by removing octodog.txt.

You can unstage files by using the git reset command. Go ahead and remove octofamily/octodog.txt.

``` terminal
- git reset octofamily/octodog.txt
```

#1.17 Undo

git reset did a great job of unstaging octodog.txt, but you'll notice that he's still there. He's just not staged anymore. It would be great if we could go back to how things were before octodog came around and ruined the party.

Files can be changed back to how they were at the last commit by using the command: git checkout -- <target>. Go ahead and get rid of all the changes since the last commit for octocat.txt
```html
- git checkout -- octocat.txt

- use : git log
	to display a log of commits w/ some details


- use : git show
```
to display all the commit messages

//PULL is a shortcut for fetching and merging


#tracking a local repo remotely
```html
- use git remote add origin git@github.com:archX3/nexus-project.git
```
to link a remote repo to the 

###then do
####to
```html
    git push -u origin master
```
####then we commit

////////////////////////////////////////////////
rm -rv 
to remove the .git to  remove the git repo

#BRANCHING

```youtrack
 - git branch
 //tells you stuff ant the branch u are currently in

 - git branch <branch-name>
 // to create a new branch

 - git checkout <branch-name>
 // to switch to another branch
```
if the branch is not already created, you can create it and switch to it at the same time w/
```html
 - git checkout -b <newBranchName>
```

#FORKING
 
 




 