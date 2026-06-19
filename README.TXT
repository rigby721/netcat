# 🚀 Custom Netcat Clone (BHP Netcat)

A lightweight, multi-platform Netcat clone written in Python 3. This tool functions as a versatile network utility designed for ethical hacking, penetration testing, and network administration. It features an interactive remote shell, command execution, and fully supports both Linux and Windows environments.

---

## ✨ Features

* Multi-Platform Support: Dynamically detects the host OS (Windows/Linux) and spawns the appropriate shell (cmd.exe or /bin/sh).
* Interactive Reverse Shell: Provides a stable remote command execution environment with a custom prompt (BHP: #>).
* Robust Exception Handling: Equipped with structural blocks to handle socket errors, improper data types, and byte-to-string conversions gracefully.
* Port Reusable Option: Implements SO_REUSEADDR to prevent port-binding lockups and "Address already in use" errors during quick restarts.

---

## 🛠️ Usage Architecture

The tool can be executed under two modes: Listener (Server) and Client (Initiator).

### 1. Listener Mode (Target System)
To set up a listener that waits for a connection and executes commands upon access:

`bash
python3 netcat.py -l -p 5555 -c -t 0.0.0.0