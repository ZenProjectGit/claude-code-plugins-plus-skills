---
name: local-tts
description: |
  Generate speech from text locally using VoxCPM2. 30 languages, voice design,
  voice cloning. Use when user asks to "say", "speak", clone a voice, or generate
  audio. Trigger phrases: "say this", "read out loud", "clone my voice",
  "generate voiceover", "text to speech". Runs 100% offline on Apple Silicon.
allowed-tools: Read, Write, Bash(cmd:*)
version: 1.0.0
author: Bubble Invest <contact@bubbleinvest.com>
license: Apache-2.0
compatible-with: claude-code
tags: [tts, voice, audio, voice-cloning, offline, apple-silicon]
---
# Local TTS — Offline Text-to-Speech

## Overview

Local text-to-speech via VoxCPM2 (2B params). Three modes: basic TTS, voice design (describe a voice in natural language), and voice cloning (3-10s reference clip). 30 languages auto-detected. Runs on Apple Silicon via Metal (MPS). Zero cost, zero cloud.

## Setup

```bash
/plugin marketplace add vdk888/local-tts
/plugin install local-tts@local-tts-marketplace
```

First use creates a Python venv and downloads ~10 GB model weights.

## Usage

```bash
VENV=~/.local-tts/venv
SCRIPT=${CLAUDE_PLUGIN_ROOT}/scripts/generate.py

# Basic TTS
"$VENV/bin/python" "$SCRIPT" --text "Hello world" --out /tmp/hello.wav

# Voice Design
"$VENV/bin/python" "$SCRIPT" --text "(warm female voice, mid-30s)Welcome back." --out /tmp/design.wav

# Voice Cloning
"$VENV/bin/python" "$SCRIPT" --text "Cloned speech." --ref /path/to/sample.wav --out /tmp/clone.wav
```

## Links

- GitHub: https://github.com/vdk888/local-tts
- Demo: https://bubble-sentinel.netlify.app/local-tts.html
