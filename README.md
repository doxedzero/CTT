# CTT
made by https://christitus.com/windows-tool/ https://github.com/ChrisTitusTech/winutil

![image](https://github.com/user-attachments/assets/947e55b4-7fdd-4676-ab92-eaa3547a67d7)

run with irm "https://christitus.com/win" | iex   (in powershell) 

or

run with bat
https://www.mediafire.com/file/8yk01kaws5vs72p/CTT.bat/files

<details>
<summary>📌 Click to view source code</summary>

```text
@echo off

REM Check for admin rights
NET FILE >nul 2>&1
IF %ERRORLEVEL% NEQ 0 (
    echo Requesting administrator privileges...
    powershell -Command "Start-Process -Verb RunAs -FilePath '%0'"
    exit /b
)

REM Execute PowerShell command as admin
echo Running Chris Titus Windows Utility...
powershell -NoProfile -ExecutionPolicy Bypass -Command "iwr -useb https://christitus.com/win | iex"

pause
```
</details>
