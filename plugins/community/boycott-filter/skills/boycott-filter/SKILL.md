---
name: boycott-filter
description: |
  Manage a personal boycott list conversationally. Chrome extension warns you
  on matching pages. Use when user complains about a brand, says "never buying
  from X again", or wants to block a company. Trigger phrases: "boycott",
  "never buying from", "block this brand", "add to boycott list".
allowed-tools: Read, Write, Bash(cmd:*)
version: 1.0.0
author: Bubble Invest <contact@bubbleinvest.com>
license: MIT
compatible-with: claude-code
tags: [boycott, chrome-extension, consumer, privacy, shopping]
---
# Boycott Filter

## Overview

Ads so intrusive they make you want to never buy the product? Tell your AI agent, it enforces the boycott. Chrome extension warns you every time you visit a boycotted brand's page. Conversational management, reason tracking, brand aliases.

## Setup

```bash
/plugin marketplace add vdk888/boycott-filter
/plugin install boycott-filter@boycott-filter-marketplace
```

## Links

- GitHub: https://github.com/vdk888/boycott-filter
