# TryHackMe — Defensive Security Intro

## 📌 Overview

**Defensive Security Intro** is an introductory TryHackMe room that demonstrates the basic role and methodology of a defensive security analyst.

The challenge uses a fictional banking application, **FakeBank**, to simulate an ongoing cyber attack and demonstrate how a defender can identify the affected user, contain the attack, investigate the attacker, create threat intelligence, and document the incident.

---

## 🎯 Objectives

- Understand the basic role of a defensive security analyst.
- Identify the username involved in the attack.
- Temporarily lock the affected user account to help contain the attack.
- Investigate information about the attacker.
- Create threat intelligence based on the investigation.
- Generate an incident report documenting the attack.

---

## 🔍 Methodology

### 1. Identify the Attacking User

I first investigated the available monitoring information to identify which username was being used during the attack.

Identifying the affected user is an important step because the account may have been compromised or used by the attacker.

### 2. Contain the Attack

After identifying the affected username, I temporarily locked the account.

This is an example of **incident containment**, where the defender takes immediate action to limit the attacker's ability to continue using the compromised account while the investigation takes place.

### 3. Investigate the Attacker

After containing the attack, I investigated the available information about the attacker.

The investigation helped determine whether the activity was associated with a known threat group and provided information that could be used to understand the attack.

### 4. Create Threat Intelligence

I used the threat intelligence system to document information about the identified attacker.

**Threat intelligence** involves collecting and analyzing information about attackers, their techniques, and their activities so that defenders can better understand and respond to threats.

### 5. Generate an Incident Report

Finally, I generated an incident report to document the attack and the actions taken during the investigation.

An incident report provides a structured record of important information such as the incident, affected account, investigation findings, containment actions, and threat intelligence.

---

## 🛠️ Tools & Techniques

| Tool / Technique | Purpose |
|---|---|
| Monitoring Dashboard | Identify and investigate suspicious activity |
| User Account Management | Temporarily lock the affected account |
| Threat Intelligence | Investigate and document information about the attacker |
| Incident Reporting | Document the security incident and response actions |

---

## 🧠 Key Lessons Learned

- Defensive security involves detecting, containing, investigating, and documenting security incidents.
- Identifying the affected username can help defenders quickly contain an attack.
- Temporarily locking a compromised account can prevent further unauthorized activity.
- Threat intelligence can provide useful information about known attackers and threat groups.
- Incident reports help security teams document what happened and how the incident was handled.
- A basic defensive workflow can be understood as **detection → containment → investigation → threat intelligence → reporting**.

---

## 🚩 Challenge Status

**Room:** Defensive Security Intro

**Learning Path:** Cyber Security 101

**Status:** Completed ✅

## 💡 Main Takeaway

> **Defensive security is not only about detecting attacks. A defender must also contain the threat, investigate the attacker, gather threat intelligence, and properly document the incident.**