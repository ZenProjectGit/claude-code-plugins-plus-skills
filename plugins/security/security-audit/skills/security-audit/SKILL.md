---
name: security-audit
description: |
  Automated security audit for Claude Code agents. Identity tamper detection,
  secret scanning, infrastructure hardening, CVE checking. Use when user asks
  to "audit security", "scan for secrets", "check CVEs", or "harden infrastructure".
  Trigger phrases: "security audit", "scan secrets", "check vulnerabilities".
allowed-tools: Read, Write, Bash(cmd:*)
version: 1.0.0
author: Bubble Invest <security@bubbleinvest.com>
license: MIT
compatible-with: claude-code
tags: [security, audit, secrets, cve, tamper-detection]
---
# Bubble Sentinel — Security Audit

## Overview

Five-module security audit: identity tamper detection (SHA-256 snapshots), infrastructure hardening (SSH, firewall, OS updates), secret scanning (17 patterns), dependency CVE checking (npm, pip, cargo), and multi-project dispatch. Python stdlib only — zero external dependencies.

## Setup

```bash
/plugin marketplace add vdk888/bubble-sentinel
/plugin install bubble-sentinel@bubble-sentinel
```

## Links

- Product page: https://bubble-sentinel.netlify.app/sentinel.html
- GitHub: https://github.com/vdk888/bubble-sentinel (private — access via subscription)
