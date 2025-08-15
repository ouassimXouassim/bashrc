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
نسخ
تحرير
sudo pacman -S fastfetch
Install yay:

bash
نسخ
تحرير
sudo pacman -S yay
⚙️ Installation
Copy the file to your home directory:

bash
نسخ
تحرير
cp bashrc.txt ~/.bashrc
Reload the configuration:

bash
نسخ
تحرير
source ~/.bashrc
To ensure the config is applied, open a new terminal or run:

bash
نسخ
تحرير
ouassim
▶️ Python Environment On/Off
To activate the default Python environment:

bash
نسخ
تحرير
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

