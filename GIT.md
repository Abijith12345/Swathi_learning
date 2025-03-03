**Git Basics: Quick Revision**  

### 1. Initialize a Repository  
```bash  
git init  
```  
Creates a new Git repository in the current directory.  

### 2. Check Status  
```bash  
git status  
```  
Shows the status of changes (untracked, staged, committed).  

### 3. Add Files to Staging  
```bash  
git add <file>    # Add a specific file  
git add .         # Add all modified & new files  
```  
Moves files from the working directory to the staging area.  

### 4. Commit Changes  
```bash  
git commit -m "Your commit message"  
```  
Saves the staged changes in the local repository.  

### 5. Push Changes to Remote Repository  
```bash  
git push origin <branch>  
```  
Sends committed changes to the remote repository (GitHub, GitLab, etc.).  

### 6. Clone a Repository  
```bash  
git clone <repo-url>  
```  
Copies a remote repository to the local system.  

### 7. Pull Latest Changes from Remote  
```bash  
git pull origin <branch>  
```  
Fetches and merges the latest changes from the remote repository.  

### 8. View Commit History  
```bash  
git log --oneline  
```  
Shows commit history in a simplified format.  

