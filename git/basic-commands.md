# Basic Commands

### **Configure Git**
Configure your Git installation (necessary for first-time setup).

```bash
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```

### **Creating a New Repository**
Start a new local repository.

```bash
cd [Folder/Repository]
git init
```

### **Cloning a Repository**
Create a local copy of a remote repository.

```bash
git clone https://github.com/username/repo.git
```

### **Checking Status**
View the status of your files (modified, staged, etc.).

```bash
git status
```

### **Adding Files**
Add files to the staging area before committing.

```bash
git add <filename>       # Add a single file
git add .                # Add all new and changed files to the staging area
```

### **Committing Changes**
Commit your staged content as a new commit snapshot.

```bash
git commit -m "Description of the commit"
```

### **Pushing Changes**
Send your commits to the remote repository on GitHub.

```bash
git push origin main    # 'main' can be replaced with your current branch name
```

### **Pulling Updates**
Fetch and merge changes on the remote server to your working directory.

```bash
git pull
```

### **Branching**
Branches are used to develop features isolated from each other.

```bash
git branch new-feature        # Create a new branch named 'new-feature'
git checkout new-feature      # Switch to the 'new-feature' branch
```

Alternatively, you can create and switch branches simultaneously:

```bash
git checkout -b new-feature
```

### **Merging**
Merge branches into your current branch.

```bash
git merge new-feature    # Merge 'new-feature' into your current branch
```

### **Checking Logs**
View changes with a log of previous commits.

```bash
git log
```

### **Undo Changes**
Revert changes to previous states.

```bash
git checkout -- <filename>   # Discard changes in the working directory
git revert <commit-hash>     # Create a new commit that undoes all of the changes made in <commit-hash>
git reset --hard <commit-hash>   # Reset your index and working directory to the state of a specific commit
```

### **Viewing Differences**
See what has changed with a detailed diff.

```bash
git diff    # View differences not yet staged
git diff --staged    # View differences between staging and the last file version
```

