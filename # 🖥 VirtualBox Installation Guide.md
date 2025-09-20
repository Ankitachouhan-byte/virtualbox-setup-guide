# 🖥 VirtualBox Installation Guide

---

## ✅ System Requirements
- [ ] Windows 10/11 (64-bit)
- [ ] 4 GB RAM minimum (8 GB recommended)
- [ ] 20 GB free disk space
- [ ] Intel VT-x/AMD-V enabled in BIOS

---

## Step 1: Install Microsoft Visual C++ Redistributable
VirtualBox requires the **Microsoft Visual C++ 2015–2022 Redistributable**.

<details>
<summary>Click to expand instructions</summary>

- Download and install both versions:
  - x64 version
  - x86 version
- Run installers → click **Install** (or **Repair** if already installed)
- **Restart your computer**

</details>

---

## Step 2: Install VirtualBox
1. Download VirtualBox from the official site:  
   [VirtualBox Downloads](https://www.virtualbox.org/wiki/Downloads)
2. Right-click on the installer (`VirtualBox-7.2.2.exe`) → **Run as administrator**
3. Follow the setup wizard → keep default options → click **Install**
4. Launch VirtualBox from the **Start Menu**

<details>
<summary>Troubleshooting</summary>

- Ensure **Visual C++ Redistributable** is installed  
- Disable **Hyper-V**: go to `optionalfeatures` → uncheck Hyper-V

</details>

---

## Step 3: Install Guest Additions (For Full Screen Ubuntu)

After Ubuntu VM is installed, run:

```bash
sudo apt update
sudo apt install build-essential dkms linux-headers-$(uname -r)
cd /media/$USER/VBox_GAs_x.x.x/
sudo ./VBoxLinuxAdditions.run

## Step 4: VirtualBox Version Check

To verify the installation:

```bash
VBoxManage --version
