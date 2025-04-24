# 🐉 RougeBSD: A Minimalist Unix-Based Pentesting Distro
## Created and maintained by **Jejo J**

**RougeBSD** is a custom Unix-like operating system built on top of **FreeBSD**, designed to be a **lightweight**, **efficient**, and **powerful** penetration testing distro for VMs and minimal hardware. Ideal for cybersecurity students, ethical hackers, and advanced users who need full control over their system — with zero bloat.

---

## 🎯 Key Features

- 🧠 **Built for Pentesting** – Comes with powerful offensive security tools.
- 🐚 **Unix Philosophy** – Minimalism and performance over fluff.
- 🖥️ **Lightweight WM** – Ultra-minimal window manager with custom keybindings.
- ⚡ **Blazing Fast** – Optimized boot time and minimal RAM usage.
- 🧱 **FreeBSD Hardened Base** – Uses jails, PF firewall, and secure configurations.
- 💾 **VM-Ready** – Runs seamlessly in VirtualBox, VMware, and QEMU.

---

## 📦 Preinstalled Tools

| Category              | Tools |
|----------------------|-------|
| **Networking**        | `nmap`, `wireshark`, `netcat`, `tcpdump` |
| **Web Pentesting**    | `burpsuite`, `wpscan`, `whatweb`, `nikto` |
| **Exploitation**      | `metasploit`, `exploitdb`, `searchsploit` |
| **Wireless Attacks**  | `aircrack-ng`, `kismet` (where supported) |
| **Development**       | `python`, `gcc`, `vim`, `git`, `make` |
| **System Tools**      | `zsh`, `htop`, `neofetch`, `tmux`, `mc` |

> Tools may be installed via `pkg`, ports, or compiled from source. Customize your installation from the base image.

---

## 🪶 Desktop Environment

- 💻 **Openbox** installed from source
- ⌨️ Minimal keyboard-driven workflows
- 🧩 St (Simple Terminal) for DWM
- 🖼️ Xorg for graphical environment
- ⚙️ Custom `~/.xinitrc` configured to launch Openbox

---

## 📁 System Footprint

- **Disk Space (Post-install):** ~3–5 GB
- **Memory Usage (Idle):** ~80–150 MB
- **Boot Time:** ~5 seconds in VM

---
## 🖼️ Gallery

> Screenshots from RougeBSD in action.

<div align="center">

<table>
  <tr>
    <td><img src="https://raw.githubusercontent.com/jejo205713/RougeBSD_OS/main/RogueBSD_images/neofetch.png" width="400"/></td>
    <td><img src="https://raw.githubusercontent.com/jejo205713/RougeBSD_OS/main/RogueBSD_images/openbox.png" width="400"/></td>
  </tr>
  <tr>
    <td><img src="https://raw.githubusercontent.com/jejo205713/RougeBSD_OS/main/RogueBSD_images/openbox2.png" width="400"/></td>
    <td><img src="https://raw.githubusercontent.com/jejo205713/RougeBSD_OS/main/RogueBSD_images/rougebsd_metasploit.png" width="400"/></td>
  </tr>
  <tr>
    <td><img src="https://raw.githubusercontent.com/jejo205713/RougeBSD_OS/main/RogueBSD_images/rougebsd_nmap.png" width="400"/></td>
    <td></td>
  </tr>
</table>

</div>

---

## 📜 Installation

### 🔧 Requirements

- VirtualBox, VMware, QEMU, or bare-metal x86_64 system
- Minimum **512MB RAM** and **5GB storage**
- Optional: `bdsinstall` script for ISO deployment

### ⚡ Quick Install via VM Image

1. Download the `RougeBSD.vmdk`,
2. Create a new VM using FreeBSD 13+ settings with 64bit arch,
3. Attach the image and boot up.
4. Login using default credentials:
   - **Username:** `root`
   - **Password:** `nyu1`

---

## 🧪 Post-Install (First Boot)

# Home-user-acc: (defaults)
- darklord : nyu1

# Enable network
```
service netif restart
service sshd start
```
# Update packages
```
pkg update && pkg upgrade
```
# Start X session - Display Manager ! 
```
startx
```


