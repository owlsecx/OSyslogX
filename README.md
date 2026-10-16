# 🦉 OSyslogX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OForensics-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OSyslogX** — System Log Daemon Configuration Hardening Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

rsyslog / syslog-ng / journald / logrotate configuration hardening auditor

---

## ✨ Features

- rsyslog legacy ($Directive / selector) + RainerScript parser, $IncludeConfig / include() following
- Forwarding over UDP / TCP / RELP without TLS, anon StreamDriverAuthMode, imudp / imtcp without ACLs
- syslog-ng network() / syslog() transport + peer-verify, program() destinations, perm(), $HOST paths, $RAWMSG
- journald Storage, retention, MaxLevelStore, Seal, limits
- logrotate retention, create modes, su / logrotten, writable postrotate scripts, olddir
- /var/log walk — auth / audit / wtmp / btmp / lastlog
- Masked secrets, --root, CWE + MITRE, TXT/MD/JSON/CSV/SARIF, self-test --demo, CI gates --fail-on / --min-severity

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OSyslogX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
