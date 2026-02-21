# Kyocera Prescribe Scripting Tool

![Batch](https://img.shields.io/badge/Batch-Windows-blue)
![Bash](https://img.shields.io/badge/Bash-Linux%20%2F%20macOS-lightgrey?logo=gnubash&logoColor=white)
![Zsh](https://img.shields.io/badge/Zsh-Advanced%20Shell-black)
![Python](https://img.shields.io/badge/Python-2.7%20%2F%203.12-blue?logo=python&logoColor=white)
![Status](https://img.shields.io/badge/Status-Archived-lightgrey)

> **Note:** This repository is archived and no longer actively maintained. It is preserved here as a portfolio reference. KCFG-related content has been removed from this public repository pending licensing clarification with Kyocera.

**Author:** Zach Reid | [zforgehub.dev](https://zforgehub.dev)

---

## Overview

A cross-platform scripting tool preloaded with common Kyocera Prescribe commands, designed for copier and printer field technicians. Built to eliminate the need to remember command syntax, locate the right text files, or understand the underlying Prescribe PDL to perform routine device operations.

The tool was written with backwards compatibility and a unified user experience in mind — regardless of which language version you run, the interface and behavior remain consistent.

---

## The Problem It Solves

Field technicians regularly need to send Prescribe commands to Kyocera devices for tasks like pulling event logs, adjusting sleep timers, or backing up device settings. Before this tool:

- Technicians had to track down the correct command text files from colleagues
- Commands had to be formatted exactly right — mistakes meant wasted paper or silent failures
- Most solutions required Admin rights or PowerShell, creating friction on managed Windows machines
- There was no single, simple tool that worked across Windows, Linux, and macOS

This tool wraps the most common commands into a simple CLI prompt that any technician can use without knowing Prescribe at all.

---

## Supported Languages

The tool is available in multiple languages to support different environments. Python is the primary maintained version; other language versions are archived as-is.

| Language | Path | Notes |
|---|---|---|
| Python | `python/` | Primary version — Python 2.7 and 3.12 |
| Batch | `batch/` | Windows `.bat` scripts |
| Bash | `bash/` | Linux/macOS (v3.2+) |
| Zsh | `zsh/` | Advanced shell (v5.x) |
| PowerShell | `ps1/` | Not implemented |

For the most up-to-date builds, see the [Releases](../../releases) page. Each language has its own branch with its latest version.

---

## Supported Commands

```
event_log          print_error_list
tiered_color_on    backup
tiered_color_off   initialize
60_lines           sleep_timer_on
66_lines           sleep_timer_off
tray_switch_on
tray_switch_off
```

---

## Usage

### Interactive (Double-Click or No Args)
Running the script with no arguments launches an interactive menu. You'll be prompted for the device IP and desired command.

### CLI Mode
All scripts accept arguments in any of the following forms:

```bash
# No args — fully interactive
prescribe.script

# IP only — prompts for command
prescribe.script 172.10.0.5

# Command only — prompts for IP
prescribe.script event_log

# Both args — no prompts
prescribe.script 172.10.0.5 event_log
prescribe.script event_log 172.10.0.5
```

### PATH Usage
A stripped-down version in `./PATH` is designed to be placed in a custom Scripts folder added to your system PATH. This allows the tool to be called from any directory via CMD without navigating to the containing folder.

---

## Status

This project is **archived**. It served its purpose and has since been superseded by more capable tooling. The repo is preserved as a reference and portfolio piece.

Active Prescribe development has continued in a separate, more fully-featured project — see [zforgehub.dev](https://zforgehub.dev) for more.

---

## Links

- 🌐 [zforgehub.dev](https://zforgehub.dev) — Portfolio & DevHub
