### Git Automation Script

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

Credits: ChatGPT for code and Eric Pogue for the idea and requirements
