# 🚀 GitHub SSH Setup Guide for Collaborators

This guide helps collaborators set up SSH for seamless pushing and pulling from our repository **without repeated username/password or token prompts**.

---

## ✅ STEP 1: Generate an SSH Key (On Each Collaborator’s Machine)

### 🖥️ On macOS, Linux, or Git Bash (Windows), run:

`` ssh-keygen -t ed25519 -C "your_email@example.com"``

If your system does not support ed25519, use RSA instead:

`` ssh-keygen -t rsa -b 4096 -C "your_email@example.com" ``

#### When prompted:

- File location: Just press Enter to accept the default (~/.ssh/id_ed25519)

- Passphrase: Optional. Leave empty for no prompt when pushing

## ✅ STEP 2: Add the SSH Key to the SSH Agent </br>
On macOS / Linux: </br>
`` eval "$(ssh-agent -s)" `` </br>
Then: </br>
`` ssh-add ~/.ssh/id_ed25519 `` </br>
On Windows (Git Bash): </br>
