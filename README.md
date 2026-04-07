### Git Automation Script
## A huge THANK YOU to Patrick O'Connor
## Warning: You may NOT copy/paste any of this code into your assignment - Eric Pogue

This project includes a Python script (`add-commit-push.py`) that automates Git operations.

[Installation Video](https://drive.google.com/file/d/1ZO6-TXmpMDEYcIZu30MidsfkfVkrUWTF/view?usp=sharing)

**Windows PowerShell**

1. Create a PowerShell profile file (if necessary):
```powershell
New-Item -Path $PROFILE -ItemType File -Force
```
2. Open PowerShell profile file:
```powershell
notepad $PROFILE
```
3. Add these lines to the .ps1 file:
```powershell
function g5 {
    Set-Location "C:\Path\to\your\project"
}

function acp {
    python3 "C:\Path\to\your\project\add-commit-push.py" @args
}

```
Now you can do:
```powershell
(something to represent your project directory)
acp -m "Updated code"
```

*Note If you get an error "Updates were rejected because the tip of your current branch is behind its remote counterpart" run*:
```powershell
git pull
```

By: Patrick O'Connor
Updated by Eric Pogue

Credits: ChatGPT for code and Eric Pogue for the idea and requirements


MacOS:
View hidden files in Finder (splat-shift-period)
Edit ".zshrc" (create it if needed)
Include updated parts of the example code below:
```bash
alias g5="/Users/ericpogue/Lewis/cpsc-20000/sprint-5"
alias acp="python3 /Users/ericpogue/Scripts/acp.py"

alias ll="ls -lhaG"
alias finder="open /System/Library/CoreServices/finder.app ."

unsetopt BEEP
```
