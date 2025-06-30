# ForkFarms Repository
##   Git Setup Guide for Studio 5000 Projects

### Software Installation: 
1. Git for Windows: git-scm.com
2. VS Code: code.visualstudio.com
3. GitHub Desktop (optional): For GUI operations

### Initial git setup: 
get config --global user.name "Your Name"
get config --global user.email "your.email@email.com"

### Create your local development folder structure:
```python
    C:\Projects\ForkFarms
        src\    #Your Studio 5000 Project Files
        docs\   #Documentation, HMI Screens, etc.
        backups\    #Manual backups (optional)
        README.md   #project description
        .gitignore  #files to be excluded from version control
```
![Local Folder View](docs/Local-Folder-View.pngLocal-Folder-View.png)

### Open repository within VSCode:
![VS Code Repo View](docs/VS-Code-Repo-View.pngVS-Code-Repo-View.png)

### In VS Code, create a new file, name it ".gitignore"
    Put the following code into the .gitignore file:
         
            #Studio 5000 temporary files
            *.tmp
            *.bak
            *~
            .DS_Store
            Thumbs.db
            
            #Backup files
            *.ACD.bak
            *.L5X.bak
             
            # Build artifactsCr
            bin/
            obj/

### Insert existing current state project files into the following buckets:
    src\ -- .ACD file, .L5X file
    docs\ -- any supporting docs (E3D, HMI, drawings, etc.)

### Initialize Git Repository:
`git init`

### Check what Git sees:
`git status`
*this shows all the files Git detected. You should see your Studio 5000 files listed as "untracked files" but no .tmp or .bak files (thanks to .gitignore file made earlier)

### Connect Local Repository to GitHub
Step 1: Create repository on GitHub
1. Go to github.com and sign in
2. Click the green "New" button (or the + icon)
3. Name your repository (e.g., MyPLCProject)
4. Don't check the "Initialize with README" (since you already have files)
5. Click "Create repository"

Step 2: Connect your local repository to GitHub

Copy these commands into VS Code terminal:

```console
git remote add origin https://github/yourusername/Projectname.git
git branch -M main
git push -u origin main
```

If curious where remote connections go, use the following instruction:
`git remote -v`

Step 3: Push your local commits:
`git push` 

### Updating Documenation & Git Nomenclature:
One of the most things to learn is Git Nomenclature, you can start to get a handle of the commands and how to interact with Git infrastructure by making changes and pushing updates to the README file (a non-critical component)

See *workflows doc here*