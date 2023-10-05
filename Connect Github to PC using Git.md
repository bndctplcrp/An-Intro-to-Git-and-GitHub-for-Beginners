# Connect Github to PC using Git

Training: The Odin Projects (https://www.notion.so/The-Odin-Projects-dae04cd679674471921d6a05eb5fc7cc?pvs=21)
Completed : No

To set your local default git branch name  from `master` to `main`

use this command

```bash
$ git config --global init.defaultBranch main
```

# Create a repository on Github

1. Go to `Repositories` section
2. click `New`
3. Input the `repository name`
4. Input `Description`
5. Choose `Public` or `Private`
6. Check `Add README file`
7. click `Create repository`

# Get files to and from Github

1. You wil redirect to `Repositories`
2. Click your repo you want to clone
3. At `code` section
4. go to `SSH`
5. copy  the link
6. Open Git Bash Application from your PC
7. Input the following command:

```bash
$ mkdir repos
```

This command creates a new directory named "repos" in your current location.

```bash
$ cd repos/
```

This command changes your current working directory to the "repos" directory you just created.

1. Time o clone your repository from Github onto your computer.
    
    Use the SSH URl you copied.  
    

```bash
$ git clone git@github.com:USER-NAME/REPOSITORY-NAME.git

EXAMPLE:
$ git clone git@github.com:bndctplcrp/git_test.git

OUTPUT:
Cloning into 'git_test'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
```

This command clones (downloads) a Git repository from the URL

You successfully connected the repository to your localmachine.

1. To test your repository in your computer use this command.

```bash
$ cd nameOfTheRepository/

Example :
$ cd git_test/

OUTPUT:
benedict policarpio@DESKTOP-NU2NS3D MINGW64 ~/repos/git_test (main)
//as you can see your corrent working directory is repos/git_test(main)

```

The command **`cd git_test/`** is used to change your current working directory to the "git_test" directory.

Once you're inside the "git_test" directory, you can perform various operations related to that directory, such as running ***Git commands***, ***creating*** or ***modifying files***, and so on.

1. Display information of you remote repository.

```bash
benedict policarpio@DESKTOP-NU2NS3D MINGW64 ~/repos/git_test (main)
$git remote -v

OUTPUT:
origin  https://github.com/username/repo.git (fetch)
origin  https://github.com/username/repo.git (push)

Sample Output:
origin  git@github.com:bndctplcrp/git_test.git (fetch)
origin  git@github.com:bndctplcrp/git_test.git (push)
```

When you run this command, it will show you the URLs of the remote repositories and their corresponding fetch and push URLs

# Use the Git workflow

1. To create a new empty file

```bash
benedict policarpio@DESKTOP-NU2NS3D MINGW64 ~/repos/git_test (main)
$ tounch nameOfFile.extension

Example:
touch hello_world.txt
```

After running this command, you will have a file named "hello_world.txt" in the same directory where you executed the command. You can then open and edit this file as needed for your project or task.

1. To display current status ofyour local Git repository.

```bash
benedict policarpio@DESKTOP-NU2NS3D MINGW64 ~/repos/git_test (main)
$ git status

OUTPUT:
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        hello_world.txt

nothing added to commit but untracked files present (use "git add" to track)
```

When you run this command, Git provides information about the state of your repository, including details about any untracked files, changes that have been made but not yet committed, and the status of your branches.

1. To stage the file for the next commit in your local Git repository .
    
    Use **`git add`,** is like preparing your changes for saving.
    

```bash
$ git add nameOfFile.extension

Example:
benedict policarpio@DESKTOP-NU2NS3D MINGW64 ~/repos/git_test (main)
$ git add hello_world.txt
```

When you run this command, you are telling Git that you want to include the changes made to "`hello_world.txt`" in the next commit. 

These changes might be the addition of a new file, modifications to an existing file, or even file deletions. Staging a file is a necessary step before committing changes in Git.

1. You can check the status of staged changes using **`git status` .**

```bash
benedict policarpio@DESKTOP-NU2NS3D MINGW64 ~/repos/git_test (main)
$ git status

OUTPUT EXAMPLE:
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   hello_world.txt
```

<aside>
🧑🏻‍🏫 The output you provided from `git status` means the following:

1. You are currently on the "`main`" branch.
2. Your local branch ("main") is up to date with the corresponding branch on the remote repository ("`origin/main`"), meaning there are no new commits on the remote that you need to fetch or integrate into your branch.
3. You have made changes that are staged and ready to be committed. Specifically, you have a new file called "hello_world.txt" that you've added to the staging area. These staged changes will become part of your next commit.

In summary, the output confirms that you have prepared the "hello_world.txt" file for a commit, and you can proceed to commit these changes using `git commit` to save them in your Git repository's history.

</aside>

1. To create a new commit in your Git repository use  `git commit -m`  .

```bash
benedict policarpio@DESKTOP-NU2NS3D MINGW64 ~/repos/git_test (main)
$ git commit -m "Add hello_world.txt"

OUTPUT EXAMPLE:
[main c30baa8] Add hello_world.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 hello_world.txt
```

It creates a snapshot of the current state of your project and records it in your Git history.

<aside>
🧑🏻‍🏫 Simplified explanation of the input:

- **`git commit`**: This is the Git command to create a commit.
- **`m`**: This flag is used to specify the commit message.
- **`"Your commit message here"`**: This is where you should provide a brief and informative message describing the changes you made in this commit. The message should be enclosed in double quotes.

</aside>

<aside>
🧑🏻‍🏫 Simplified explanation of the output:

- `[main c30baa8] Add hello_world.txt`: This means you took a picture (commit) of your project, and you gave it a title ("Add hello_world.txt"). The "main" is like a chapter in your project's history book, and "c30baa8" is a unique code for this snapshot.
- `1 file changed, 0 insertions(+), 0 deletions(-)`: This tells you that you made a change to one thing (a file), but you didn't add or remove anything from it. You just created a new file.
- `create mode 100644 hello_world.txt`: This confirms that you added a new file called "hello_world.txt" to your project.

In short, you've added a "snapshot" of your project with a new file called "hello_world.txt" to your Git history. It's like taking a photo and giving it a title to remember what you did.

</aside>

1. You can use `git status` again  to  check the status of staged changes.

```bash
benedict policarpio@DESKTOP-NU2NS3D MINGW64 ~/repos/git_test (main)
$ git status

OUTPUT:
On branch main
Your branch is ahead of 'origin/main' by 1 commit.//
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

<aside>
🧑🏻‍🏫 `"Your branch is ahead of 'origin/main' by 1 commit"`: This means that your local "main" branch has one more commit than the remote branch called 'origin/main.' In other words, you have made a new commit locally that hasn't been pushed to the remote repository yet.

</aside>

1. The **`git log`** output you provided shows the commit history of your Git repository.

```bash
benedict policarpio@DESKTOP-NU2NS3D MINGW64 ~/repos/git_test (main)
$ git log

OUTPUT:

commit c30baa8ca5a8abe0e09662913ca1f19323825984 (HEAD -> main)
Author: bndctplcrp <benedictpolicarpio08@gmail.com>
Date:   Wed Oct 4 23:26:05 2023 +0800

    Add hello_world.txt

commit f250aa505596e9595a97412b40e11b922f2bcbd1 (origin/main, origin/HEAD)
Author: BENEDICT POLICARPIO <142641358+bndctplcrp@users.noreply.github.com>
Date:   Wed Oct 4 23:11:00 2023 +0800

    Initial commit

```

# ****Modify a file****

1. To open the current directory in VS code.

```bash
benedict policarpio@DESKTOP-NU2NS3D MINGW64 ~/repos/git_test (main)
$ code .
```

When you run this command in your terminal, it launches VS Code and opens the files and folders located in your current working directory, which, in your case, is the "git_test" directory.

1. You can now modify add files in your repo.
    
    Example make a `README.md` file and save the file with  **`Ctrl** + **S**`
    

1. You can use your Visual code to input the commands using built-in terminal. Pressing **`Ctrl** + **`**` (backtick)

1. Use the  `git status`  in VS built-in Terminal to check the status of staged changes.

```bash
INPUT:
PS C:\Users\bened\repos\git_test> git status

OUTPUT:
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md
no changes added to commit (use "git add" and/or "git commit -a")
```

1. Use **`git add .`** to stage all changes in your current working directory (and its subdirectories) for the next commit.

```bash
INPUT:
PS C:\Users\bened\repos\git_test> git add .

OUTPUT:
On branch main
Your branch is ahead of 'origin/main' by 1 commit.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md
        modified:   hello_world.txt
```

This command is used to stage all changes in your current working directory (and its subdirectories) for the next commit. The dot (**`.`**) represents the current directory, so you are staging all changes in your project.

or 

Use  `git add <file>...` 

```bash
PS C:\Users\bened\repos\git_test> git add README.md
```

1. After running **`git add .` or** `git add <file>` you can use **`git status`** to confirm that the changes you want to commit have been successfully staged.

```bash
git status
```

1. Finally, you can proceed to create a commit that includes the staged changes using the **`git commit`** command:

```bash
git commit -m "Your commit message here"

OUTPUT:
[main 8901dff] Edit README.md and hello_world.txt
 2 files changed, 4 insertions(+), 1 deletion(-)

```

1. Then, type `git status` once again, which will output “*nothing to commit*”.

```bash
INPUT:
PS C:\Users\bened\repos\git_test> git status

OUTPUT:
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

1. Take one last look at your commit history by typing `git log`. You should now see three entries.

```bash
INPUT:
PS C:\Users\bened\repos\git_test> git log

OUTPUT:
commit 8901dff33d00dd71cc396b4593b632a612c1e673 (HEAD -> main)
Author: bndctplcrp <benedictpolicarpio08@gmail.com>
Date:   Wed Oct 4 23:34:19 2023 +0800

    Edit README.md and hello_world.txt

commit c30baa8ca5a8abe0e09662913ca1f19323825984
Author: bndctplcrp <benedictpolicarpio08@gmail.com>
Date:   Wed Oct 4 23:26:05 2023 +0800

    Add hello_world.txt

commit c30baa8ca5a8abe0e09662913ca1f19323825984
Author: bndctplcrp <benedictpolicarpio08@gmail.com>
Date:   Wed Oct 4 23:26:05 2023 +0800

    Add hello_world.txt

commit f250aa505596e9595a97412b40e11b922f2bcbd1 (origin/main, origin/HEAD)
Author: BENEDICT POLICARPIO <142641358+bndctplcrp@users.noreply.github.com>
Date:   Wed Oct 4 23:11:00 2023 +0800

    Initial commit
```

# Push your work to Github

1. To upload and synchronize your local repository's commits and branches with a remote repository use   `git push` or  `git push origin main`.

```bash
INPUT:
benedict policarpio@DESKTOP-NU2NS3D MINGW64 ~/repos/git_test (main)
$ git push

OUTPUT:
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (7/7), 662 bytes | 662.00 KiB/s, done.
Total 7 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:bndctplcrp/git_test.git
   f250aa5..8901dff  main -> main
```

or

```bash
INPUT:
benedict policarpio@DESKTOP-NU2NS3D MINGW64 ~/repos/git_test (main)
$ git push origin main

OUTPUT:
Everything up-to-date
```

<aside>
🧑🏻‍🏫 Certainly, let's simplify it:

- `git push origin main`: This command explicitly tells Git to push your local changes from the "main" branch to the remote repository named "origin."
- `git push`: This shorthand command assumes you want to push your current branch to a remote repository named "origin." It's convenient when the local and remote branches have the same name.

In short, `git push origin main` is more specific about what and where you're pushing, while `git push` assumes you want to push your current branch to the remote repository named "origin."

</aside>

1. Type `git status` one final time. It should output “*Your branch is up to date with ‘origin/main’. nothing to commit, working tree clean*”.

```bash

INPUT:
benedict policarpio@DESKTOP-NU2NS3D MINGW64 ~/repos/git_test (main)
$ git status

OUTPUT:
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

1. Go to your repository  on Github account. You will see all the updates (files) that you pushed from your local machine.

![Untitled](Connect%20Github%20to%20PC%20using%20Git%2096e9ae80145f4de99c76158a36707070/Untitled.png)