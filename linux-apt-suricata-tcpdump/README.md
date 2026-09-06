# Lab: Install software on Linux with APT

## Goal
Practice using APT on a Debian-based Linux system to install, remove, and reinstall security tools.

## Tools
- APT: package manager for Debian-based distros
- Suricata: network threat detection (IDS/IPS)
- tcpdump: command-line packet capture

## Commands I used
```
apt
sudo apt update
sudo apt install suricata
sudo apt install tcpdump
sudo apt remove suricata
sudo apt install suricata
```
## What I learned
- Debian-family systems use .deb packages and APT.
- Update package lists before installing.
- Removing and reinstalling a package is normal troubleshooting.
- Suricata watches traffic for threats; tcpdump captures packets.

## What I would check next on a real alert
- Is the host Debian-based (apt) or Red Hat-based (yum)?
- Was the package list updated first?
- After installation, is the tool present and able to run?
- For tcpdump: which interface am I capturing, and do I have permission?

## Scope
Completed in a course lab environment, not on a company network.
