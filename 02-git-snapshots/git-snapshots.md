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
