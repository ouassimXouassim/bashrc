# bashrc
# ~/.bashrc - The Ultimate Arch Linux Edition (Customized) # A single, powerful, and easy-to-manage configuration file.


# 🖥️ The Ultimate Arch Linux Bash Configuration

A professional Bash configuration file for Arch Linux and BlackArch, containing **the best settings, shortcuts, and helper functions** to boost productivity and speed up terminal workflow.

---

## 📌 Features
- **Professional Kali-like Prompt** with:
  - Time & date display
  - Last command execution time
  - Git branch support
  - Python virtual environment display
- **Advanced history settings** with instant sync across all terminals
- **Comprehensive Aliases** for Pacman, Yay, system management, and navigation
- **Helper Functions** like:
  - `mkcd` — create a directory and cd into it
  - `extract` — extract almost any archive type
  - `blackarch` — list installed BlackArch categories and tools
- **Built-in command guide** via the `help` command
- Integration with **fastfetch / neofetch** for system info at login
- Easy Python virtual environment activation/deactivation (`on` / `off`)

---

## 📦 Requirements

Before using this file, make sure you have:
- **Bash** (installed by default on Arch Linux)
- **Pacman** (default package manager for Arch)
- **Yay** (for AUR packages) — optional
- **fastfetch** or **neofetch** (to display system info)
- **Python** + a virtual environment located at:
  ```bash
  ~/.venvs/global/
broot (optional — for file navigation)

Install fastfetch:

bash

sudo pacman -S fastfetch
Install yay:

bash

sudo pacman -S yay
⚙️ Installation
Copy the file to your home directory:

bash

cp bashrc.txt ~/.bashrc
Reload the configuration:

bash
source ~/.bashrc
To ensure the config is applied, open a new terminal or run:

bash
ouassim
▶️ Python Environment On/Off
To activate the default Python environment:

bash

on
To deactivate the Python environment:

bash


off
📚 Custom Commands (Aliases)
Command	Description
update	Update system using Pacman
yupdate	Update system + AUR using yay
install	Install a package
remove	Remove a package
search	Search for a package in repositories
ll	List files with details
mkcd	Create a directory and enter it
extract	Extract almost any archive type
blackarch	Show installed BlackArch categories/tools
publicip	Show public IP address
weather	Show weather in terminal
ouassim	Reload .bashrc file

For more commands, type:

bash


help
📸 Prompt Preview
text


┌──(user㉿host)-[/path/to/dir](branch)
├──[14:35 2025-08-15]
└──✔ $
✔ means last command succeeded

✘ means last command failed

Python venv name is shown if active
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
create venu enverment in /home/user/.venvs/global/
active   on 
desactive off
===========================================================================
run  help for more info 
=================================
## 🗂️ Aliases Reference

Below is the full list of aliases included in this Bash configuration:

| Alias            | Command                                                                                                                       | Description                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| **System / Packages (Pacman & Yay)** |
| `update`         | `sudo pacman -Syu`                                                                                                             | Update system using Pacman                                                  |
| `install`        | `sudo pacman -S`                                                                                                               | Install a package                                                           |
| `remove`         | `sudo pacman -Rns`                                                                                                             | Remove a package with unused dependencies                                  |
| `search`         | `pacman -Ss`                                                                                                                   | Search packages in repositories                                             |
| `orphans`        | `pacman -Qdtq`                                                                                                                 | List orphaned packages                                                      |
| `clean`          | `sudo pacman -Rns $(pacman -Qdtq)`                                                                                             | Remove all orphaned packages                                                |
| `yupdate`        | `yay -Syu --devel`                                                                                                             | Update system + AUR (including development packages)                        |
| `yinstall`       | `yay -S`                                                                                                                       | Install from AUR or official repos                                          |
| `yclean`         | `yay -Yc`                                                                                                                      | Clean all unneeded dependencies from AUR                                   |
| `upall`          | `sudo pacman -Syu && yay -Syu`                                                                                                 | Update system + AUR together                                                |
| `pacsearch`      | `pacman -Ss`                                                                                                                   | Search for packages                                                         |
| `pacinfo`        | `pacman -Si`                                                                                                                   | Show package information                                                    |
| `psize`          | `pacman -Qi | grep Installed`                                                                                                  | Show installed package sizes                                                 |
| **Navigation** |
| `..`             | `cd ..`                                                                                                                        | Go up one directory                                                          |
| `...`            | `cd ../..`                                                                                                                     | Go up two directories                                                        |
| `....`           | `cd ../../..`                                                                                                                  | Go up three directories                                                      |
| `cdp`            | `cd ~/Pictures`                                                                                                                | Go to Pictures folder                                                        |
| `cdd`            | `cd ~/Downloads`                                                                                                               | Go to Downloads folder                                                       |
| `cdt`            | `cd ~/tools`                                                                                                                   | Go to tools folder                                                           |
| `cdo`            | `cd ~/Documents`                                                                                                               | Go to Documents folder                                                       |
| `ll`             | `ls -lAh`                                                                                                                      | List files with details                                                      |
| `la`             | `ls -A`                                                                                                                        | List hidden files without `.` and `..`                                      |
| `l`              | `ls -CF`                                                                                                                       | Compact list view                                                            |
| **System Management & Monitoring** |
| `c`              | `clear`                                                                                                                        | Clear terminal screen                                                        |
| `cls`            | `clear`                                                                                                                        | Clear terminal screen                                                        |
| `h`              | `history`                                                                                                                      | Show command history                                                         |
| `meminfo`        | `free -m -l -t`                                                                                                                 | Show memory usage                                                            |
| `cpuinfo`        | `lscpu`                                                                                                                         | Show CPU information                                                         |
| `psmem`          | `ps auxf | sort -nr -k 4 | head -10`                                                                                            | Show top 10 processes by memory usage                                        |
| `pscpu`          | `ps auxf | sort -nr -k 3 | head -10`                                                                                            | Show top 10 processes by CPU usage                                           |
| `se`             | `sudo systemctl`                                                                                                               | Manage system services                                                       |
| `se-u`           | `systemctl --user`                                                                                                              | Manage user services                                                         |
| `ip`             | `ip a`                                                                                                                          | Show network interfaces and IP addresses                                     |
| `ports`          | `ss -tuln`                                                                                                                      | Show open ports                                                               |
| `pingg`          | `ping google.com`                                                                                                               | Ping Google                                                                   |
| `publicip`       | `curl ifconfig.me`                                                                                                              | Show public IP address                                                        |
| `weather`        | `curl wttr.in`                                                                                                                  | Show weather forecast in terminal                                             |
| **Quick Config File Editing** |
| `dns`            | `sudo nano /etc/resolv.conf`                                                                                                    | Edit DNS configuration                                                       |
| `mirrorlist`     | `sudo nano /etc/pacman.d/mirrorlist`                                                                                            | Edit Pacman mirror list                                                       |
| `pacmanconf`     | `sudo nano /etc/pacman.conf`                                                                                                    | Edit Pacman configuration                                                    |
| `hosts`          | `sudo nano /etc/hosts`                                                                                                          | Edit hosts file                                                               |
| `hostnamefile`   | `sudo nano /etc/hostname`                                                                                                       | Edit system hostname                                                          |
| `netconf`        | `sudo nano /etc/NetworkManager/NetworkManager.conf`                                                                             | Edit NetworkManager configuration                                            |
| `fstab`          | `sudo nano /etc/fstab`                                                                                                          | Edit filesystem table                                                         |
| `mkinit`         | `sudo nano /etc/mkinitcpio.conf`                                                                                                | Edit mkinitcpio configuration                                                |
| `bootloader`     | `sudo nano /boot/loader/entries/arch.conf`                                                                                      | Edit bootloader entry                                                         |
| `iptables`       | `sudo nano /etc/iptables/iptables.rules`                                                                                        | Edit iptables firewall rules                                                  |
| `passwdfile`     | `sudo nano /etc/passwd`                                                                                                         | Edit passwd file                                                              |
| `shadow`         | `sudo nano /etc/shadow`                                                                                                         | Edit shadow file                                                              |
| `sudoers`        | `sudo EDITOR=nano visudo`                                                                                                       | Edit sudoers file                                                             |
| `locale`         | `sudo nano /etc/locale.gen`                                                                                                     | Edit locale configuration                                                     |
| `environment`    | `sudo nano /etc/environment`                                                                                                    | Edit environment variables                                                    |
| `x11conf`        | `sudo nano /etc/X11/xorg.conf.d/00-keyboard.conf`                                                                               | Edit X11 keyboard configuration                                               |
| `gpgconf`        | `sudo nano /etc/pacman.d/gnupg/gpg.conf`                                                                                        | Edit GPG configuration                                                        |
| **Personal / Custom Shortcuts** |
| `ouassim`        | `source ~/.bashrc`                                                                                                              | Reload Bash configuration                                                     |
| `ouassim-edite`  | `sudo mousepad ~/.bashrc`                                                                                                       | Edit Bash configuration                                                       |
| `music`          | `ncmpcpp`                                                                                                                       | Launch ncmpcpp music player                                                    |
| `win`            | `mountpoint -q /mnt/windows || (sudo mkdir -p /mnt/windows && sudo mount -t ntfs-3g /dev/sda3 /mnt/windows); cd /mnt/windows`   | Mount and access Windows partition                                            |
| `on`             | `source ~/.venvs/global/bin/activate`                                                                                          | Activate Python virtual environment                                           |
| `off`            | `deactivate`                                                                                                                    | Deactivate Python virtual environment                                         |

help

