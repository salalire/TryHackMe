# TryHackMe — Linux Fundamentals (Pt1)

## 📌 Overview

**Linux Fundamentals (Pt1)** is an introductory TryHackMe room that teaches the basics of interacting with a Linux terminal.

The room covers essential Linux commands, navigation, searching, and **shell operators** used to control how commands work together.

---

## 🎯 Objectives

- Understand basic Linux terminal usage.
- Navigate the Linux filesystem.
- Search for files and information.
- Understand shell operators.
- Learn the difference between `>`, `>>`, `&`, and `&&`.

---

## 🔍 Methodology

### 1. Interact with the Linux Terminal

I used the terminal to execute Linux commands and interact with the system.

The terminal allows users to manage files, navigate directories, search for information, and execute programs.

### 2. Navigate the Filesystem

I practiced moving between directories and viewing files using basic Linux commands.

Common commands include:

    pwd
    ls
    cd
    cat

These commands are essential for navigating and understanding a Linux environment.

### 3. Search for Information

I learned how Linux provides different ways to search for files and information.

For example:

    find
    grep

These commands are useful when investigating a system or looking for specific files or text.

### 4. Output Redirection: `>` vs `>>`

I learned that `>` and `>>` are used to redirect command output into a file.

#### `>`

The `>` operator **overwrites** the existing contents of a file.

Example:

    echo "Hello" > file.txt

If `file.txt` already contains data, its previous contents are replaced.

#### `>>`

The `>>` operator **appends** output to the end of an existing file.

Example:

    echo "World" >> file.txt

The existing contents remain, and `World` is added to the end.

The main difference is:

    >   = overwrite
    >>  = append

### 5. Running Commands in the Background: `&`

The `&` operator runs a command in the **background**, allowing the shell to continue accepting commands.

Example:

    command &

This is useful when I want a command or process to continue running while I perform other tasks in the terminal.

### 6. Conditional Command Execution: `&&`

The `&&` operator allows multiple commands to be executed sequentially, but the next command runs **only if the previous command succeeds**.

Example:

    command1 && command2

This means:

    Run command1
          ↓
    Did it succeed?
       ↓       ↓
      Yes      No
       ↓       ↓
    command2   Stop

This is useful when the second command depends on the first command completing successfully.

---

## 🛠️ Tools & Techniques

| Tool / Operator | Purpose |
|---|---|
| Linux Terminal | Execute commands and interact with the system |
| `pwd` | Display the current directory |
| `ls` | List files and directories |
| `cd` | Navigate between directories |
| `cat` | Display file contents |
| `find` | Search for files |
| `grep` | Search for text |
| `>` | Redirect output and overwrite a file |
| `>>` | Redirect output and append to a file |
| `&` | Run a command in the background |
| `&&` | Run the next command only if the previous succeeds |

---

## 🧠 Key Lessons Learned

- Linux systems can be controlled efficiently through the terminal.
- `>` redirects output and **overwrites** a file.
- `>>` redirects output and **appends** to a file.
- `&` runs a command in the **background**.
- `&&` executes the next command only when the previous command **succeeds**.
- Shell operators allow multiple commands and processes to be controlled efficiently.

---

## 🚩 Challenge Status

**Room:** Linux Fundamentals (Pt1)

**Learning Path:** Cyber Security 101

**Status:** Completed ✅

---

## 💡 Main Takeaway

> **Understanding Linux shell operators is essential because they control how commands interact, redirect output, and execute processes.**