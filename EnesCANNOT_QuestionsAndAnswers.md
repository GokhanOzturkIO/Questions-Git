## 1) What is Git?

Git is the most widely used version control system in the world. It is a free and open-source distributed version control system that records changes made to code over time in a special database called a repository. Git allows users to track project history, see who made changes and when, and revert the project to an earlier state if necessary. It is popular due to its speed, scalability, and efficient handling of branching and merging operations. Git enables developers to collaborate on projects, with each team member having a copy of the project with its history on their machine, allowing for local saving of project snapshots and synchronization with others even if the central server is offline.

---

## 2) What is the difference between "git pull" and "git fetch" commands?

`git fetch` downloads new data from a remote repository without integrating it into your working files, allowing you to review the changes before integrating them into your local repository.

`git pull`, on the other hand, downloads new data and directly integrates it into your current working copy files, which can be faster but also introduces changes and conflicts into your local repository.

`git fetch` is safer as it only downloads new data, while `git pull` integrates it into your current working copy files, which can cause conflicts and changes that require manual resolution.

---

## 3) If our teammate says "I sent my codes, continue with my development" and we cannot get the codes she/he sent to our local location with "git pull", what could be a mistake?

If your teammate says that she/he has sent her/his codes, but you are unable to get those codes locally with git pull, there could be several reasons for this. Here are some common mistakes to check:

- **Repository not pushed to remote:** 
Ensure that your teammate has pushed her changes to the remote repository. If not, you will not be able to get those changes with git pull.

- **Incorrect branch name:** 
Check that you are using the correct branch name for your teammate's code. You can use git branch -a to see a list of all available branches.

- **Permissions issue:** 
Check if there are any permission issues with the remote repository. If you don't have the necessary permissions to pull changes, you will not be able to get the latest changes.

By checking for these common mistakes, you can identify and resolve any issues with getting your teammate's latest changes with git pull.

---

## 4) What does "origin" in the "git fetch origin" command correspond to?

In the command "git fetch origin", "origin" represents the default name assigned to the remote repository from which you want to fetch changes. It is typically the alias given to the original repository URL when you clone a Git repository. This allows you to refer to the remote repository using a short and memorable name.

---

## 5) What does the word "HEAD" represent?

"HEAD" is a special pointer that points to the current location in the Git repository. It usually shows the latest commit of the current working copy or branch, but can also be temporarily redirected to a different location. This can be used to mark different commits, tags or references.

---

## 6) What exactly is a "Staging Area" or "Index"?

The "Staging Area" or "Index" acts as an intermediate zone between Git's workspace and the repository. This area is used to process changes and prepare them for the next commit. Changes are first made in the workspace and then added to the "Staging Area". This area allows checking changes before commit and gives developers the flexibility to organize changes.

---

## 7) What does "untracked file" mean?

"Untracked file" refers to files that Git does not track. These are files for which Git does not track or save changes. Newly created or modified files are not automatically tracked by Git and are therefore called "Untracked". These files are ignored by Git during the next commit. If you want to track them or save their changes, you must first add the files to the "Staging Area". This ensures that the files will be tracked by Git and saved in subsequent commits.

---

## 8) What happens if we delete the ".git" folder?

Deleting the `.git` folder in a Git repository will remove all the version control history and settings associated with that repository, making the local repository a standard folder with no version control history or settings. However, if the repository has been pushed to a remote server, we can still download a new copy of the repository with all the version control history and settings by cloning or downloading it again.

---

## 9) What should we do if we want a "ReadMe.md" file to be automatically created every time we use the "git init" command in our own local area?

We can use 2 different ways to solve this type of request:

- 1.1 First of all, we open a folder to keep our git template anywhere.
     ```bash
     mkdir ~/.git-templates
     ```
- 1.2 Afterwards, we write our template content to a file and add it to the git templates folder we opened.
     ```bash
     echo "# My Project" > ~/.git-templates/ReadMe.md
     ```
- 1.3 Finally, we update the git configuration and set the init.templatedir property to point to your own custom template directory.
     ```bash
     git config --global init.templatedir ~/.git-templates
     ```
--
- 2.1 As in the previous solution, we need to have a template here too. Assuming we have a template, I move on to the next step.
- 2.2 In this step, we have a template like this and we give it as a parameter when we initialize git.
     ```bash
     git init --template=~/.git-template
     ```
---

## 10) What is the "branch" structure mentioned in Git? What does it provide us?

In Git, a "branch" is used to manage different versions of a project. Each branch allows the development of a different feature or change. This allows working on multiple features at the same time and isolates risks. It also provides benefits such as parallel development and history preservation.

---

## 11) How can we create a "branch" from scratch?

We can create a branch from scratch as follows:

```bash
git branch branch_name
```

and to move from the existing branch to the newly created branch, we write the following command:
```bash
git checkout branch_name
```

--

Or briefly, we can switch to the branch we just created as follows:
```bash
git checkout -b branch_name
```

---

## 12) How can we switch to an existing "branch"?

Here's how to switch to an existing branch:
```bash
git checkout branch_name
```

---
## 13) When using the "git clone" command, if we only want to pull a specific branch, how can we do it?

When using the git clone command, if we only want to pull a specific branch, we can use the --single-branch option along with the --branch or -b option to specify the branch we want to clone. Here's how to do it:

```bash
git clone --single-branch --branch branch_name repository_url
```

---

## 14) What does "merge conflict" mean?

Merge Conflict occurs when Git fails to automatically merge changesets during the merge process. This usually happens when different developers change the same lines in the same files, or when changes in different branches overlap. Merge conflicts give developers the opportunity to review and resolve changes in files where conflicts exist.

---

## 15) What information can we see with the "git log" command?

This command displays the commit history for the current branch, starting with the most recent commit. The output includes the commit hash, author, date, and commit message.

For example;
```
commit 56f5f077c5b14a3b90f028f79699e75d15ee0b02 (HEAD -> EnesCANNOT)  
Author: Enes CAN <enesscann98@gmail.com>
Date:   Tue Feb 6 21:21:16 2024 +0300

    The question "What does "merge conflict" mean?" has been answered.
```

---

## 16) How many different changes between two situations can we see with "git diff"?

With the "git diff" command, we can see the differences between two different states of our Git repository. There are several ways to use this command, but the most common usage is to compare the current state of our working directory with the latest commit. This will show us any changes we have made since the last commit.
</br>
Here is an example of how we might use the "git diff" command:
```
git diff HEAD
```
This command will show us the differences between the latest commit and the current state of our working directory.
</br>
If we want to compare two specific commits, we can use the following command:
```
git diff commit1 commit2
```
This will show us the differences between the two specified commits.
</br>
If we want to compare a specific commit with the current state of our working directory, we can use the following command:
```
git diff commit1
```
This will show us the differences between the specified commit and the current state of our working directory.
</br>
If we want to compare two specific branches, we can use the following command:
```
git diff branch1 branch2
```
This will show us the differences between the two specified branches.
</br>
If we want to compare a specific branch with the current state of our working directory, we can use the following command:
```
git diff branch1
```
This will show us the differences between the specified branch and the current state of our working directory.
</br>
In all of these cases, the output will show us the differences between the two states, including any added, modified, or deleted files.

---

## 17) What do we get back with git reset?

The git reset command is used to revert changes to the Git repository. The way changes are rolled back is determined by using options such as --soft, --mixed and --hard.

git reset --soft: This option reverts the last commit but leaves the changes in the working directory and staging area.
```
git reset --soft HEAD
```

git reset --mixed: This option reverts the last commit and keeps the changes in the working directory, but reverts the staging area.
```
git reset --mixed HEAD
```

git reset --hard: This option completely reverts the last commit and changes made.
```
git reset --hard HEAD
```

---

### 18) What is the difference between "git commit" and "git push"?

The "git commit" command records changes in the local Git repository, creating a new commit with a message describing the changes. These changes are stored locally and are not shared with others. On the other hand, the "git push" command sends the commits made locally to a remote repository, allowing them to be shared with others. These commands are used together to share local changes and collaborate with others.

---

## 19) What does atomic commit mean?

An atomic commit in Git is a single commit that contains all the changes made to the repository at a particular point in time. The term "atomic" comes from the field of computer science, and it refers to an operation that is indivisible and uninterruptible. In Git, atomic commits are used to ensure that the repository remains in a consistent state, which makes it easier to undo changes and restore the repository to a known, stable state. It is generally a good practice to use atomic commits whenever possible, especially when working on a shared repository.

---

## 20) What does repository mean?

Repository is where a project's files and version history are stored. It acts as a central hub for developers to collaborate, track changes, and manage the project's codebase. Each repository contains files, commit history, branches, and tags, and can exist locally or remotely for distributed development.

---

## 21) What is "git tag"? How is it different from "git branch"?

In Git, a tag is a marker that is used to identify a specific commit in the repository, and it does not change once it is created. A branch, on the other hand, is a movable pointer to a commit, and it can be updated to point to different commits. The main difference between tags and branches is that tags are fixed and do not change, while branches are movable and can be updated. Tags are typically used to identify important commits, while branches are used to develop new features or bug fixes.

---

