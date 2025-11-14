LXC/LXD Auto Installer 🚀
A beautiful, feature-rich bash script for automated LXC and LXD installation on Ubuntu and Debian systems. This installer provides an exceptional user experience with advanced animations, comprehensive error handling, and professional output.

https://img.shields.io/badge/LXC-LXD-blue
https://img.shields.io/badge/Bash-4.0%252B-green
https://img.shields.io/badge/Platform-Ubuntu%2520%257C%2520Debian-orange
https://img.shields.io/badge/License-MIT-lightgrey

✨ Features
🎨 Visual Enhancements
8 Different Spinner Styles - Dots, circle, pulse, bounce, arrow, moon, triangle, clock

Multiple Progress Bars - Block, dot, arrow, pulse styles with smooth animations

Rainbow Color Effects - Beautiful color transitions in headers

Dynamic Box Drawing - Multiple border styles (single, double, round, bold)

Typewriter Text Effects - Animated text display

Responsive Design - Adapts to terminal size

🛡️ Robust Error Handling
Comprehensive Logging - Detailed logs at /tmp/lxd_installer.log

Retry Mechanism - Automatic retries with configurable attempts

System Validation - Checks memory, disk space, and dependencies

Graceful Interruption - Proper handling of Ctrl+C

Detailed Error Messages - Line numbers, commands, and solutions

🔧 Technical Features
Automatic Dependency Resolution - Handles all required packages

Existing Installation Detection - Skips already installed components

System Requirement Checks - Validates minimum resources

Privilege Verification - Ensures proper sudo access

Post-Installation Validation - Verifies LXD functionality

🚀 Quick Start
Prerequisites
Ubuntu 18.04+ or Debian 10+

Bash 4.0 or higher

Sudo privileges

Minimum 2GB RAM (recommended)

Stable internet connection

Installation
bash
# Download the script
wget https://raw.githubusercontent.com/HopingBoyz/lxc-lxd-installer/main/lxd-installer.sh

# Make it executable
chmod +x lxd-installer.sh

# Run the installer
./lxd-installer.sh
One-Liner Installation
bash
curl -sL https://raw.githubusercontent.com/HopingBoyz/lxc-lxd-installer/main/lxd-installer.sh | bash
📋 What Gets Installed
Core Packages
LXC - Linux Containers

LXD - Container hypervisor

Snapd - For LXD installation

Dependencies:

bridge-utils

uidmap

squashfs-tools

curl, wget

Configuration
LXD initialization with interactive setup

User added to LXD group

Proper permissions setup

Storage and network configuration

🎮 Usage
After installation, you can start using LXC/LXD immediately:

bash
# List all containers
lxc list

# Launch a Ubuntu container
lxc launch ubuntu:24.04 my-container

# Access the container
lxc exec my-container -- bash

# Stop the container
lxc stop my-container

# List available images
lxc image list images:
🛠️ Advanced Usage
Manual LXD Configuration
If you need to reconfigure LXD later:

bash
sudo lxd init
Checking Installation Logs
bash
tail -f /tmp/lxd_installer.log
Verifying Installation
bash
# Check LXD service status
lxc info

# Test container functionality
lxc list

# Check storage pools
lxc storage list
🔧 Troubleshooting
Common Issues
Permission Denied

bash
# Re-login or reload groups
newgrp lxd
# Or reboot
sudo reboot
Snapd Not Ready

The script automatically retries

Manual fix: sudo systemctl restart snapd

Insufficient Resources

Ensure at least 2GB RAM and 5GB free disk space

The script will warn about low resources

Network Issues

bash
# Check LXD network
lxc network list
lxc network show lxdbr0
Log Files
Installation log: /tmp/lxd_installer.log

LXD logs: /var/snap/lxd/common/lxd/logs/

🎨 Customization
Environment Variables
bash
# Set maximum retry attempts
export MAX_RETRIES=5

# Set retry delay in seconds
export RETRY_DELAY=10
Script Options
The script automatically detects:

Operating system and version

System architecture

Available resources

Existing installations

📊 System Requirements
Component	Minimum	Recommended
OS	Ubuntu 18.04 / Debian 10	Ubuntu 22.04+ / Debian 11+
RAM	2GB	4GB+
Storage	5GB free	20GB+ free
Architecture	x86_64, ARM64	x86_64
🤝 Contributing
We welcome contributions! Please feel free to submit pull requests, report bugs, or suggest new features.

Development
Fork the repository

Create a feature branch

Make your changes

Test thoroughly

Submit a pull request

Testing
Please test on:

Ubuntu 20.04, 22.04, 24.04

Debian 10, 11, 12

📝 Changelog
[1.0.0] - 2024-01-01
Initial release

Advanced animations and UI

Comprehensive error handling

Ubuntu and Debian support

🙏 Acknowledgments
LXC/LXD Team - For the amazing container technology

Linux Community - For continuous support and feedback

Contributors - Everyone who helped improve this installer

📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

⚠️ Disclaimer
This script is provided as-is with no warranties. Always test in a non-production environment first. The authors are not responsible for any damages or issues caused by using this script.

<div align="center">
Made with ❤️ by HopingBoyz

Report Bug · Request Feature

</div>
🔗 Useful Links
LXD Official Documentation

LXC/LXD GitHub

Linux Containers

Snapcraft

🐛 Reporting Issues
If you encounter any issues:

Check the log file: /tmp/lxd_installer.log

Check existing issues

Create a new issue with:

OS version

Error message

Log file snippet

Steps to reproduce
