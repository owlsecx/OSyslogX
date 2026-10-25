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


OSyslogX is an offline, read-only auditor for system-log daemon configurations: rsyslog, syslog-ng, systemd-journald and logrotate. It parses legacy rsyslog directives and RainerScript, syslog-ng network transports, journald storage/retention and logrotate rules, flagging insecure forwarding, missing TLS and weak retention. Secrets are masked, findings are mapped to CWE and MITRE, and reports export to TXT, Markdown, JSON, CSV or SARIF.

---

## ✨ Features


- rsyslog legacy ($directive/selector) and RainerScript parser with include() following
- Detects forwarding over UDP/TCP/RELP without TLS and imudp/imtcp inputs without ACLs
- syslog-ng network()/syslog() transport and peer-verify, program() destinations and path checks
- journald Storage/retention/Seal and logrotate retention, create modes, su and writable postrotate scripts
- /var/log permission walk (auth, audit, wtmp, btmp, lastlog) with masked secrets
- CWE+MITRE mapping, --root offline trees and TXT/MD/JSON/CSV/SARIF export with CI gates

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage


```bash
./OSyslogX --scan -f sarif -o syslog.sarif
./OSyslogX --rsyslog /etc/rsyslog.conf --journald /etc/systemd/journald.conf
./OSyslogX -r /mnt/image --fail-on high --json
./OSyslogX --demo
./OSyslogX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
