# 🔥 RougeBSD: A Minimalist BSD-Based Pentesting Distro

**RougeBSD** is a custom Unix-like operating system built on top of FreeBSD, designed to be a **lightweight**, **efficient**, and **powerful** penetration testing distro for VMs and minimal hardware. Ideal for cybersecurity students, ethical hackers, and advanced users who need full control over their system, with no bloat.

---

## 🎯 Key Features

- 🧠 **Built for Pentesting** – Comes with powerful offensive security tools.
- 🐧 **Unix Philosophy** – Minimalism and performance are prioritized over fluff.
- 🖥️ **Lightweight WM (DWM)** – Ultra-minimal window manager with custom keybindings.
- ⚡ **Blazing Fast** – Optimized boot time and minimal RAM usage.
- 🧱 **FreeBSD Hardened Base** – Using jails, PF firewall, and secure configurations.
- 💾 **VM-Ready** – Runs seamlessly in VirtualBox, VMware, and QEMU.

---

## 📦 Preinstalled Tools

| Category              | Tools |
|----------------------|-------|
| **Networking**        | `nmap`, `wireshark`, `netcat`, `tcpdump` |
| **Web Pentesting**    | `burpsuite`, `wpscan`, `whatweb`, `nikto` |
| **Exploitation**      | `metasploit`, `exploitdb`, `searchsploit` |
| **Reconnaissance**    | `recon-ng`, `theHarvester`, `dnsenum` |
| **Password Attacks**  | `hydra`, `john`, `hashcat`, `crunch` |
| **Wireless Attacks**  | `aircrack-ng`, `kismet` (where supported) |
| **Post Exploitation** | `empire`, `netexec`, `socat`, `pupy` |
| **Development**       | `python`, `gcc`, `vim`, `git`, `make` |
| **System Tools**      | `zsh`, `htop`, `neofetch`, `tmux`, `mc` |

> Tools may be installed via `pkg`, ports, or compiled from source. You can customize your installation from the base image.

---

## 🪶 Desktop Environment

- 💻 **DWM (Dynamic Window Manager)** installed from source
- ⌨️ Minimal keyboard-driven workflows
- 🧩 St (Simple Terminal) for DWM
- 🖼️ Xorg for graphical environment
- ⚙️ Custom `~/.xinitrc` for launching DWM

---

## 📁 System Footprint

- **Disk Space (Post-install):** ~3-5 GB
- **Memory Usage (Idle):** ~80-150 MB
- **Boot Time:** ~5 seconds in VM

---

## 📜 Installation

### 🔧 Requirements

- VirtualBox, VMware, QEMU, or bare-metal x86_64
- At least **512MB RAM** and **5GB storage**
- Optionally: `bdsinstall` script for ISO deployment

### ⚡ Quick Install via VM Image

1. Download the `RougeBSD.vmdk` or ISO file.
2. Create a VM with FreeBSD 13+ settings.
3. Attach disk or ISO and boot up.
4. Login using default credentials:
   - **Username:** `root`
   - **Password:** `rougebsd`

### 🧪 Post-Install (First Boot)

```sh
# Enable network
service netif restart
service sshd start

# Update packages
pkg update && pkg upgrade

# Start X session
startx
```

## Bug Reports:
Please report any bugs via email: [jejo205713@gmail.com](mailto:jejo205713@gmail.com)
