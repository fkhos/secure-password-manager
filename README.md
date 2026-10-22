# secure-password-manager
🛡️ Secure CLI Password Manager
A professional-grade, local-first password management system built using Linux (WSL/Ubuntu), GPG encryption, and Git version control.

🚀 Overview
This project demonstrates a secure workflow for managing sensitive data using the standard Linux pass utility. By using Elliptic Curve Cryptography (Curve25519), this system ensures that passwords are encrypted locally before ever being synced to a remote repository.

🛠️ Tech Stack & Skills
Operating System: Linux (Ubuntu via WSL2)

Encryption: GPG (GNU Privacy Guard) - Curve25519

Version Control: Git & GitHub

Shell: Bash 

🔐 Security Features
Asymmetric Encryption: Uses a GPG public/private key pair. Even if the GitHub repository is public, the data is useless without the private key and master passphrase.

Zero-Knowledge Sync: Passwords are encrypted on the machine. GitHub only hosts the encrypted blobs (.gpg files), never the plain text.

Secure Clipboard: Integration with xclip to copy passwords for 45 seconds before auto-clearing.

📖 How It Works
GPG Key Generation: Created a highly secure ECC key for encryption.

Initialization: Linked the password store to a specific GPG fingerprint.

Git Integration: Initialized a local Git repo to track changes and history.

GitHub Sync: Established a secure connection using Personal Access Tokens (PAT) for remote backup.

🛠️ Usage Examples
Bash
# To view the password tree
pass

# To add a new secure entry
pass insert Work/LinkedIn

# To copy an encrypted password to clipboard
pass -c Work/LinkedIn

# To sync changes to GitHub
pass git push

👨‍💻 Portfolio Takeaways
This project was built to showcase my proficiency in:

-Managing encryption keys and digital identities.

-Navigating the Linux filesystem and CLI environments.

-Implementing secure DevOps workflows for sensitive data.
