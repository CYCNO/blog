---
title: Connect Github Account To Git Using GPG Key
author: cycno
date: 2024-02-10 01:10:00 +0530
categories: [git, github, account]
tags: [connect, git, github, gpg, account]
pin: true
math: true
mermaid: true
image:
  path: https://imgs.search.brave.com/_o1kCH3UVBqNdw-_r7EbIVzo7fnmz1TWhEodhS764JA/rs:fit:860:0:0/g:ce/aHR0cHM6Ly9jZG4u/YW5hbHl0aWNzdmlk/aHlhLmNvbS93cC1j/b250ZW50L3VwbG9h/ZHMvMjAyNC8wMS9p/bWFnZS0yMDEucG5n
  lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
  alt: Responsive rendering of Chirpy theme on multiple devices.
---

Git is a distributed version control system used to track changes in source code during software development. It allows multiple developers to collaborate on projects efficiently.

### Installation

To install Git, follow these steps:

1. **Windows:**

   - Download the installer from [git-scm.com](https://git-scm.com/).
   - Run the installer and follow the prompts.

2. **macOS:**

   - Git should be pre-installed. If not, you can install it via Homebrew:
     ```bash
     brew install git
     ```

3. **Linux (Debian/Ubuntu):**
   - Install Git via apt:
     ```bash
     sudo apt install git
     ```

### Configuration

After installing Git, configure your username and email:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

## Introduction to GitHub

GitHub is a platform that hosts Git repositories and facilitates collaboration among developers. It offers features like pull requests, issue tracking, and project management.

### Creating a GitHub Account

To create a GitHub account:

1. Go to [github.com](https://github.com/) in your web browser.
2. Click on "Sign up" and follow the instructions to create your account.

### Setting up a Repository

To create a new repository on GitHub:

1. Log in to your GitHub account.
2. Click on the "+" icon in the top-right corner and select "New repository."
3. Fill in the repository name, description, and choose visibility settings.
4. Click "Create repository."

### Cloning a Repository

To clone a repository from GitHub to your local machine:

```bash
git clone <repository_url>
```

## Setting Up GPG Key with GitHub

Using GPG (GNU Privacy Guard) keys adds an extra layer of security to your commits by verifying your identity.

### Generating a GPG Key

To generate a GPG key:

```bash
gpg --full-generate-key
```

Follow the prompts to set up your key, including selecting the key type and key size, and providing your name and email.

### Adding the GPG Key to GitHub

1. Export your GPG key:

   ```bash
   gpg --armor --export <key_id>
   ```

2. Copy the GPG key output.

3. Go to your GitHub account settings.

4. Click on "SSH and GPG keys" in the left sidebar.

5. Click "New GPG key" and paste your key.

6. Click "Add GPG key."

### Verifying Commits

To sign your commits with your GPG key:

1. Set your GPG key for signing:

   ```bash
   git config --global user.signingkey <key_id>
   ```

2. Enable commit signing:
   ```bash
   git config --global commit.gpgsign true
   ```

Now, when you commit changes, they will be signed with your GPG key.

## Conclusion

You've now learned the basics of Git, GitHub, and setting up GPG key for signing commits. Happy coding! 🚀
