### Creating Snapshots

The first effective thing to know while learning git is, how to take a snapshot of your project

- **Initializing a repo**

  - First to initialize a git repo, we have to create a directory in our system and we have to change current directory to newly created one

  ```bash
  mkdir learn-git
  cd mkdir
  ```

  - Next is to initialize a git repository in current path (learn-git) in our example. The below command will initialize a empty repository in (learn-git) folder

  ```bash
  git init
  ```

- **Git Workflow**

  - In our daily basis, we will have a project directory (local machine) and we have a git repository (which is actually a hidden repository in our project directory = .git), we can see the hidden repository using `ls -a` command.
  - Now everyday according to our tasks, we modify files in our project directory, and when the state of project changes we take snapshot, commit those changes in to repository — creating a commit is taking a snapshot of our project
  - In git, we have special intermediate step between modifying and committing. It’s called the **staging area -** It is place where we are proposing the changes for our next commit or next snapshot.
  - So, when we modify our changes, we add our changes to staging area, review our changes, and then if everything is correct - then we commit those changes. The proposed snapshot will be permanently stored in our repository
  - So in short, staging area allows us to review our work before recording a snapshot. If some of the changes shouldn’t be recorded a part of next snapshot, we can un-stage them and commit them as part of next snapshot
  - Now, let’s see the commands to achieve the git workflow explained above

- **Adding Modified files to staging area**

  - We add modified changes to staging area using

    ```bash
    git add .   #add entire project to repo recursively
    git add file1.md file2.md  #add specific files seperated by space
    ```

- **Committing to repository from staging area**

  - Now our files are in staging area. This is the stage we are proposing for the next commit. we review our changes, and then commit the changes to permanently store them in the repository

    ```bash
    git commit -m "intial commit" #-m option is message we provide to that commit
    ```

    NOTE:

    1. After committing our changes, our staging area does not become empty. Our staging area is same snapshot that we have in our repository.

    2. Each commit in a repository is a snapshot of what we have in staging area
