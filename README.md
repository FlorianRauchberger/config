# macOS Setup

This repository is a reusable starting point for setting up a new Mac. It installs a standard collection of command-line tools and desktop applications with Homebrew, configures the GitHub CLI, and can clone all repositories available from a GitHub account.

## What is included

- `install.sh` installs the Xcode Command Line Tools, applies the `Brewfile`, and updates installed Homebrew packages.
- `Brewfile` defines the Homebrew taps, command-line tools, development utilities, and macOS applications to install.
- `pull_all_repos.sh` authenticates with GitHub and clones all repositories accessible to the authenticated account.


## Prerequisites

- A [GitHub account](https://github.com/)
- [Homebrew](https://brew.sh/) installed and available as `brew`

Install Homebrew if it is not already available:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## Set up a new Mac

Clone this repository and enter its directory:

```bash
git clone https://github.com/FlorianRauchberger/config.git
cd config
```

Review the `Brewfile` before installation and remove anything you do not want. Then run:

```bash
bash install.sh
```

## Clone repositories from GitHub

The Homebrew bundle installs the GitHub CLI (`gh`). From the directory where you want your repositories to be stored, run:

```bash
bash /path/to/config/pull_all_repos.sh
```

