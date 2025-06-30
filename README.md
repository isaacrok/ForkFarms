# ForkFarms
# Git Setup Guide for Studio 5000 Projects

#Software Installation: 
1. Git for Windows: git-scm.com
2. VS Code: code.visualstudio.com
3. GitHub Desktop (optional): For GUI operations

Initial git setup: 
get config --global user.name "Your Name"
get config --global user.email "your.email@email.com"

Create your local development folder structure:
    C:\Projects\ForkFarms
        src\    #Your Studio 5000 Project Files
        docs\   #Documentation, HMI Screens, etc.
        backups\    #Manual backups (optional)
        README.md   #project description
        .gitignore  #files to be excluded from version control

![alt text](Local-Folder-View.png)

Open repository within VSCode:
![alt text](VS-Code-Repo-View.png)

In VS Code, create a new file, name it ".gitignore"
    Put the following code into the .gitignore file:
`**            # Studio 5000 temporary files
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
            obj/**`

Insert existing current state project files into the following buckets:
    src\ -- .ACD file, .L5X file
    docs\ -- any supporting docs (E3D, HMI, drawings, etc.)

Initialize Git Repository:
`    ```console
    git init
    ````'

Check what  