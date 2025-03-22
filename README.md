# Mastering Batch Scripting: A Comprehensive Guide

## Introduction

Batch scripting is a powerful way to automate repetitive tasks in Windows. This tutorial covers everything from basic commands to advanced automation techniques.

---

## Chapter 1: Getting Started with Batch Scripting

### 1.1 What is a Batch Script?

A batch script is a text file containing a sequence of commands to be executed by the Windows Command Prompt.

### 1.2 Creating and Running a Batch Script

1. Open **Notepad**.
2. Write your *com*mands (e.g., `echo Hello, World!`).
3. Save the file with a `.bat` extension (e.g., `script.bat`).
4. Double-click the `.bat` file to execute it.

### 1.3 Basic Commands

- `echo` - Displays text in the command prompt.
- `cls` - Clears the command prompt screen.
- `pause` - Pauses execution and waits for user input.
- `exit` - Closes the command prompt.

---

## Chapter 2: File and Directory Operations

### 2.1 Creating, Renaming, and Deleting Files

- `echo Hello > file.txt` (Creates a file and writes text)
- `ren file.txt newfile.txt` (Renames a file)
- `del newfile.txt` (Deletes a file)

### 2.2 Working with Directories

- `mkdir foldername` (Creates a new folder)
- `rmdir foldername /s /q` (Deletes a folder and its contents)
- `cd foldername` (Navigates into a directory)

---

## Chapter 3: Automating Application Launch

### 3.1 Opening Applications

- `start notepad` (Opens Notepad)
- `start chrome` (Opens Google Chrome if installed in PATH)

### 3.2 Opening Specific Files with Applications

- `start notepad myfile.txt` (Opens a text file in Notepad)
- `start "" "C:\Path\To\App.exe"` (Opens any application)

### 3.3 Automating Browser with Multiple Tabs

```bat
start "" "C:\Program Files\Google\Chrome\Application\chrome.exe" ^
    "https://chat.openai.com" ^
    "https://mail.google.com" ^
    "https://www.indeed.com" ^
    "https://www.linkedin.com"
```

### 3.4 Opening VS Code and Git Bash

```bat
start "" code
start "" "C:\Program Files\Git\git-bash.exe"
```

---

## Chapter 4: Conditional Statements and Loops

### 4.1 Using IF Statements

```bat
@echo off
set /p name=Enter your name:
if "%name%"=="Admin" echo Welcome, Admin!
```

### 4.2 Using Loops

```bat
@echo off
for %%i in (1 2 3 4 5) do echo Number %%i
```

---

## Chapter 5: Advanced Batch Scripting Techniques

### 5.1 Logging Outputs to a File

```bat
@echo off
echo Script started at %date% %time% >> log.txt
echo Running task... >> log.txt
echo Script completed. >> log.txt
```

### 5.2 Scheduling Batch Scripts to Run Automatically

Use **Task Scheduler**:

1. Open Task Scheduler (`taskschd.msc` from Run window).
2. Click **Create Basic Task**.
3. Choose **Trigger** (e.g., on system startup).
4. Choose **Action** → Start a Program.
5. Select your `.bat` file and finish.

---

## Conclusion

This guide provides a solid foundation in batch scripting, from basic commands to automating tasks. Experiment with different commands and create useful automation scripts!

