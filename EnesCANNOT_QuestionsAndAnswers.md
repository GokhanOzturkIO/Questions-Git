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

