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

---

### ⚡ Quick Install via VM Image

1. Download the `RougeBSD.vmdk` (it will be compressed as `.zst`),
2. Create a new VM using FreeBSD 13+ settings with 64-bit architecture,
3. Attach the image and boot up.
4. Login using default credentials:
   - **Username:** `root`
   - **Password:** `nyu1`

---

### 📦 Decompress `.zst` VM Image on Windows

If you downloaded a `.zst` compressed image, here's how to extract it:

#### ✅ Option 1: **GUI (Easy) — Use PeaZip**
- Download PeaZip from: [https://peazip.github.io](https://peazip.github.io)
- Right-click the `.zst` file → “Extract here”

#### ✅ Option 2: **Command Line (Power Users)**
1. Download the Zstandard tool from [https://github.com/facebook/zstd/releases](https://github.com/facebook/zstd/releases)
2. Open `cmd` or `PowerShell` in the folder containing `zstd.exe` and your image
3. Run:
   ```bash
   zstd -d RougeBSD.vmdk.zst

### 🐧 Decompress `.zst` VM Image on Linux

If you're on Linux and downloaded a `.zst` compressed image:

#### 📦 Method 1: Using `zstd` (CLI)

1. Install `zstd` if not already available:

   ```bash
   sudo apt install zstd        # Debian/Ubuntu
   sudo dnf install zstd        # Fedora/RHEL
   sudo pacman -S zstd          # Arch

2.Decompress the file with this command:
```bash
zstd -d RougeBSD.vmdk.zst
```

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


