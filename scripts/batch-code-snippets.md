---
title: Windows Batch
tags: Development Resource Environment Script Batch Code Snippets
---

## Code Snippets

### Check for user with Administrator privileges

```batch
REM Check for user with Administrator privileges
net session >NUL 2>&1
IF %ERRORLEVEL% EQU 0 (
GOTO :GO_execute
) ELSE (
ECHO.
ECHO   ERROR: "User has NOT Administrator Privileges" 
ECHO   Please, run this script with Administrator Privileges 
ECHO   Installation Aborted...
ECHO.
Pause
GOTO :EOF
)
:GO_execute
```
