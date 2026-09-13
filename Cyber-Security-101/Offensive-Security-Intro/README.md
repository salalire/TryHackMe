# TryHackMe — Offensive Security Intro

## 📌 Overview

**Offensive Security Intro** is an introductory TryHackMe room that demonstrates the basic mindset and methodology used in offensive security.

The challenge uses a fictional banking application, **FakeBank**, to demonstrate how an attacker can enumerate a web application, discover hidden functionality, and identify weaknesses in access control.

---

## 🎯 Objectives

- Understand the basic mindset of an offensive security practitioner.
- Perform basic web application enumeration.
- Discover hidden pages and directories.
- Identify a hidden administrative page.
- Understand the importance of authentication and authorization.

---

## 🔍 Methodology

### 1. Explore the Web Application

I first interacted with the FakeBank web application to understand its available functionality and identify potential areas that could be investigated further.

### 2. Directory Enumeration

I used the `dirb` command/tool to perform directory enumeration against the target web application.

The purpose of directory enumeration is to discover directories and pages that may not be linked from the main website.

Example:

    dir <target>

Directory enumeration can reveal resources such as:

    /admin
    /login
    /uploads
    /backup

### 3. Discover the Admin Page

The enumeration revealed an administrative page that was not directly exposed through the normal website interface.

This demonstrated that simply hiding a page or not displaying a link to it does **not** provide effective security.

### 4. Analyze the Access Control

The administrative functionality should only be accessible to an authenticated and authorized administrator.

A secure application should verify the user's permissions on the server before allowing access to protected resources.

The important distinction is:

- **Authentication:** Who are you?
- **Authorization:** What are you allowed to access?

Therefore, knowing or discovering an administrative URL should not be enough to access its functionality.

---

## 🛠️ Tools & Techniques

| Tool / Technique | Purpose |
|---|---|
| Web Browser | Interact with the target web application |
| `dir` | Enumerate directories and hidden web resources |
| Directory Enumeration | Discover additional application endpoints |
| Access-Control Testing | Check whether restricted resources are properly protected |

---

## 🧠 Key Lessons Learned

- Attackers often begin by **enumerating** the target application.
- Directory enumeration can reveal hidden pages and functionality.
- A hidden URL is **not** a security control.
- Authentication verifies a user's identity.
- Authorization determines what that authenticated user is allowed to access.
- Sensitive functionality must be protected with proper **server-side authorization checks**.

---

## 🚩 Challenge Status

**Room:** Offensive Security Intro

**Learning Path:** Cyber Security 101

**Status:** Completed ✅

## 💡 Main Takeaway

> **Never rely on hiding a URL to protect sensitive functionality. Proper authentication and authorization must be enforced by the application.**