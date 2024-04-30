---
theme: serif
title: "CSCI 297: Ethical Hacking"
info: "Introduction: Linux Basics and Cryptographic Tools"
author: William J. Tolley
email: "wtolley@wlu.edu"
date: "Today's Date"
highlighter: shiki
transition: slide
---

# Introduction: Linux Basics and Cryptographic Tools

**CSCI 297: Ethical Hacking**

---

# About Me

- Just a guy

---

# Course Overview

## What is Hacking?

Definition:
: "Hacking is the practice of exploring and manipulating systems or networks in ways that deviate from their intended purposes."

Examples of Hacking Activities:
- Reverse Engineering Binaries
- Network Exploitation and Packet Spoofing
- Cryptography and Encryption Techniques
- Memory and Disk Forensics
- Circumvention of Censorship and Surveillance

Key Concept:
: "Being naughty is fun!"

---

# Campus Prohibited Activities

**According to university policy, the following activities are prohibited:**

- Unauthorized access or disclosure of confidential information
- Misrepresentation of identity
- Tampering with computer configurations
- Impeding network traffic

For more details, refer to the [University's Computing Resources Policy](https://my.wlu.edu/general-counsel/code-of-policies/confidentiality-and-information-security/computing-resources-network-website-and-email-use-policy).

---

# Course Objectives

In this course, we will:
- Practice Unauthorized Access
- Master Identity Misrepresentation
- Tamper with Computer Configurations
- Disrupt Network Traffic

---

# Linux Introduction

## Why Linux for Ethical Hacking?

- Stability, flexibility, and control
- Prevalence in server environments
- Strong community and resource availability

---

# Basic Linux Commands

- Terminal introduction
- Command line navigation: `ls`, `cd`, `mkdir`, `pwd`
- Managing files and directories

---

# Interactive Game: Bashcrawl

```bash
# Start Bashcrawl
cd bashcrawl
./start_game.sh


---
theme: serif
title: "CSCI 297: Ethical Hacking"
info: "Introduction: Linux Basics and Cryptographic Tools"
author: William J. Tolley
email: "wtolley@wlu.edu"
date: "Today's Date"
highlighter: shiki
transition: slide
---

# Introduction to Arch Linux

- Arch Linux is a lightweight and flexible Linux distribution designed for simplicity and customization.
- Follows a rolling-release model, meaning continuous updates keep your system current.
- Emphasizes simplicity and minimalism, providing users with the freedom to build their system exactly how they need it.

---

# Pacman Package Manager

- Pacman is the package manager used in Arch Linux.
- It provides efficient package management and dependency resolution.
- Simple commands like `pacman -S package` can be used to install new packages.

---

# Arch User Repository (AUR)

- The AUR is a community-driven repository for Arch users, providing a vast collection of user-contributed packages.
- While the AUR offers a wide range of packages, users should exercise caution and review PKGBUILD scripts for security and compatibility before installation.

---

# Rolling Release Model

- Arch Linux follows a rolling-release model, which means no fixed release cycles.
- This model ensures that users always have access to the latest software and security patches.
- While it offers the latest software, users should be cautious during updates to avoid potential system breakages.

---

# Viewing the Arch Linux Keyring

```bash
# View the Arch Linux keyring
pacman-key --list-keys

---

# Understanding the Keyring

- **Keyring Use**: Holds cryptographic keys for package management and authentication.
- **Functionality**: Contains keys used to sign official packages in Arch Linux, ensuring their authenticity and integrity.
- **Management**: Users can view, manage, and verify keys to maintain system security.

---

# Introduction to Encryption (PGP)

## Importance of Pretty Good Privacy (PGP)

- **Purpose**: Encrypts data for secure communication and storage.
- **Methodology**: Uses public-key cryptography for cryptographic privacy and authentication.
- **Applications**: Widely used for digital signatures, secure email communications, and file encryption.

---

# Introduction to Cryptography

- **Significance**: Essential in securing communications and protecting data from unauthorized access.
- **Types**: Differentiates between symmetric and asymmetric encryption.
- **Real-world Use**: Extensively applied in securing internet communications and protecting sensitive data.

---

# What is the Web of Trust?

## Concept

- **Web of Trust (WoT)**: A decentralized trust model used in PGP to establish the credibility of public key bindings.
- **Purpose**: Allows users to endorse the identity of key owners, thus extending trust.

## Functionality

- **Operation**: Users sign each other’s public keys to verify and trust the owner's identity.
- **Network Building**: This endorsement helps others in the network decide whom to trust.

---

# Generating PGP Keys with GnuPG

```bash
# Command to generate a new ECC key for signing and encrypting
gpg --full-generate-key

- When prompted for the kind of key you want, choose "(9) ECC (sign and encrypt)".
- Select "Curve 25519