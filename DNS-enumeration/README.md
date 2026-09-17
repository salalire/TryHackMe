# TryHackMe — DNS Enumeration Challenge

## 📌 Overview

This challenge focuses on **DNS enumeration** using the `dig` command.

The target machine at `10.129.183.39` was also running a DNS server. The goal was to query this DNS server and retrieve the flag stored in a DNS record for `givemetheflag.com`.

---

## 🎯 Objectives

* Identify the DNS server provided by the challenge.
* Use `dig` to perform DNS queries.
* Understand the difference between the default DNS resolver and a specific DNS server.
* Query the target DNS server directly.
* Retrieve the flag from the DNS response.

---

## 🔍 Methodology

### 1. Perform a Normal DNS Query

First, I queried the domain using the default DNS resolver:

```
dig givemetheflag.com
```

The query returned:

```
status: NXDOMAIN
```

The response also showed:

```
SERVER: 127.0.0.53#53
```

This indicated that my system was using the local DNS stub resolver at `127.0.0.53`.

The domain was not resolved through this DNS server.

### 2. Query the Target DNS Server

The challenge provided the target DNS server:

```
10.129.183.39
```

Instead of using the default resolver, I directly queried the target DNS server using the `@` symbol:

```
dig @10.129.183.39 givemetheflag.com
```

This time, the query was successful:

```
status: NOERROR
```

The response contained a `TXT` record:

```
givemetheflag.com.  0  IN  TXT  "flag{0767ccd06e79853318f25aeb08ff83e2}"
```

### 3. Identify the Flag

The flag was stored inside the DNS `TXT` record.

The retrieved flag was:

```
flag{0767ccd06e79853318f25aeb08ff83e2}
```

---

## 🧠 Key Concepts

### `dig`

`dig` is a command-line tool used to query DNS servers and retrieve DNS records.

Basic usage:

```
dig DOMAIN
```

For example:

```
dig givemetheflag.com
```

By default, `dig` uses the DNS resolver configured on the system.

### Querying a Specific DNS Server

The `@` symbol allows `dig` to query a specific DNS server.

Syntax:

```
dig @DNS_SERVER DOMAIN
```

In this challenge:

```
dig @10.129.183.39 givemetheflag.com
```

This instructed `dig` to send the DNS query directly to `10.129.183.39`.

### DNS TXT Record

DNS supports different types of records, including `A`, `AAAA`, `MX`, `NS`, and `TXT`.

A `TXT` record stores text associated with a domain.

In this challenge, the flag was stored inside a `TXT` record:

```
IN  TXT  "flag{0767ccd06e79853318f25aeb08ff83e2}"
```

---

## 🛠️ Tools & Techniques

| Tool / Technique    | Purpose                                   |
| ------------------- | ----------------------------------------- |
| `dig`               | Perform DNS queries                       |
| `@10.129.183.39`    | Query the specified DNS server directly   |
| DNS                 | Resolve domain names and retrieve records |
| `TXT` Record        | Retrieve text stored in DNS               |
| `givemetheflag.com` | Domain queried during the challenge       |

---

## 🧠 Key Lessons Learned

* DNS queries normally use the system's configured DNS resolver.
* The `SERVER` field in `dig` output shows which DNS server responded to the query.
* `127.0.0.53` is commonly used as a local DNS stub resolver on Linux systems.
* The `@` symbol in `dig` allows a specific DNS server to be queried directly.
* DNS does not only contain IP address records; it can also contain `TXT` records and other types of information.
* When a normal DNS query fails, it is useful to query the intended DNS server directly.

---

## 🚩 Challenge Status

**Challenge:** DNS Enumeration — Retrieve the Flag

**Target:** `10.129.183.39`

**Domain:** `givemetheflag.com`

**Status:** Solved ✅

---

## 🏁 Flag

```
flag{0767ccd06e79853318f25aeb08ff83e2}
```

---

## 💡 Main Takeaway

> **When performing DNS enumeration, always consider which DNS server is answering your query. A domain may return no results through your default resolver while providing useful records when queried directly against the target DNS server.**
