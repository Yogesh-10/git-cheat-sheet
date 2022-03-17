### **What Is Git and Why is it so popular?**

- Git is the most popular version control system among many others.
- A version control system records changes made to our code overtime, in a special database called repository
- we can see the version history, who has made what changes, when and why.
- and if we mess something up in our code, we can easily revert back to previous state
- So in simple words, with git we can track our history and work/collaborate together

### **Types of version control system - Centralized and distributed**

- **Centralized**
  - In a centralized system all team members connect to a centralized server to get the latest copy of the code and to share change with others
  - The problem with centralized system is the single point of source - if the server goes down, we cannot collaborate or save snapshots of our project
  - Eg: Subversion, Team Foundation Server
- **Distributed**
  - In distributed system, every team members has a copy of the project with the same history on their machine, so we can save snapshots of our project locally on our machine.
  - if the server goes down, we can sync our code by directly connecting with others
  - Eg: Git, Mercurial, Bit Bucket

### Git Configs

- The first time we use git, we have to specify few configuration such as name, email. we can set this configuration on three different levels
  - System - All Users
  - Global - All repo of current users
  - local - current repository

```bash
git config --global user.name "Your user name"
git config --global user.email "Your email"
```

- We can also set configs for CRLF - Carriage return and Line feed

```bash
git config --global core.autocrlf true //for windows
git config --global core.autocrlf input //for mac
```
