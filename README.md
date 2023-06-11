# Bitcoin Core Node Builder

Create a secure Bitcoin Core node with ease.

NOTE: This code is still under development and not yet ready. Test at your own risk. You can track progress under the Minimum Viable Product milestone.

## What Does This Script Do?

The script performs the following actions:
1. Install system updates and reboot if necessary.
2. Download, cryptographically validate, configure, and run Bitcoin Core.
3. Create a shortcut to Bitcoin Core on the desktop.
4. Prevent system sleep, suspend, and hibernate.
5. While the initial block download completes, display relevant info including the percent synced (e.g. 34%) and free disk space left.
6. TODO: After the initial block download completes, enable Tor and I2P. (This step isn't ready yet.)
7. After the initial block download completes, tell the user that the script is finished and to press any key to close the terminal window.

## What Files Does This Script Touch?

The script modifies the following files:
- Anything affected by upgrading the system and installing dependencies
- `$HOME/bitcoin-*-x86_64-linux-gnu.tar.gz`, the downloaded Bitcoin Core compressed tarball
- `$HOME/SHA256SUMS`, the tarball's checksum file
- `$HOME/SHA256SUMS.asc`, the signatures for the checksum file
- `$HOME/guix.sigs/`, 
- `$HOME/bitcoin/`, a user-definable extraction directory
- `$HOME/.bitcoin/`, the default Bitcoin Core data directory
- `$HOME/.bitcoin/bitcoin.conf`, the Bitcoin Core configuration file

## Prerequisites

A fresh install of [Ubuntu Desktop](https://ubuntu.com/tutorials/install-ubuntu-desktop) or other Debian-based Linux distribution with an internet connection enabled.

This script **does not** support macOS, 32-bit systems, or Arm-based systems.

## How to Start Bitcoin Core Node Builder

NOTE: This code is still under development and not yet ready. Test at your own risk. You can track progress under the Minimum Viable Product milestone.

1. Install git.
    ```bash
    sudo apt install -y git
    ```
2. Clone the repository.
    ```bash
    git clone https://github.com/epiccurious/bitcoin-core-node-builder.git
    ```
3. Run the script.
    ```bash
    bitcoin-core-node-builder/nodebuilder.sh
    ```
