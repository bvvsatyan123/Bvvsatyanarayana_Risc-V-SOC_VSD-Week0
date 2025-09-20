# Bvvsatyanarayana_Risc-V-SOC_VSD-Week0

# 🚀 RISC-V Reference SoC Tapeout Program – Toolchain Setup

![Ubuntu](https://img.shields.io/badge/Ubuntu-20.04+-orange?logo=ubuntu)
![Tools](https://img.shields.io/badge/Tools-Yosys%2C%20GTKWave%2C%20Icarus%20Verilog-blue)
This repository contains the tool installation guide and verification screenshots for the **VSD RISC-V Reference SoC Tapeout Program**.

---

## ✅ System Requirements

- **OS**: Ubuntu 20.04 or later (64-bit)
- **RAM**: 6 GB
- **Disk Space**: 50 GB
- **CPU**: 4 vCPU

---

## 🔧 Ubuntu VirtualBox Setup (Optional)

For Ubuntu users running in VirtualBox:

```bash
sudo apt update
sudo apt install build-essential dkms linux-headers-$(uname -r)
cd /media/$USER/VBox_GAs_*/   # Adjust if needed
sudo ./autorun.sh
````

This enables auto screen resizing and drag-drop between host and VM.

---

## 🧰 Toolchain Installation

### 🛠️ 1. Yosys – Synthesis Tool

```bash
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git
cd yosys

sudo apt install make build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 \
    libboost-system-dev libboost-python-dev libboost-filesystem-dev zlib1g-dev

make config-gcc
git submodule update --init --recursive
make -j$(nproc)
sudo make install
```

---

### 🛠️ 2. Icarus Verilog – Simulation Tool

```bash
sudo apt-get update
sudo apt-get install iverilog
```

---

### 🛠️ 3. GTKWave – Waveform Viewer

```bash
sudo apt-get update
sudo apt install gtkwave
```

---

## ✅ Tool Verification

After installing, verify each tool:

```bash
yosys             # Should launch yosys shell
iverilog -v       # Should show version info
gtkwave -v        # Should show GTKWave version
```

### 📸 Screenshots

* **Yosys**
  ![Yosys Launch](https://github.com/user-attachments/assets/fafe55bf-af95-4934-b3d0-4f20e8381909)

* **Icarus Verilog**
  ![Icarus Verilog Version](images/iverilog.jpg)

* **GTKWave**
  ![GTKWave Version](images/gtkwave.jpg)

---

## 📁 Recommended Project Structure

```bash
your-repo/
├── README.md
├── images/
│   ├── yosys.jpg
│   ├── iverilog.jpg
│   └── gtkwave.jpg

```

---

## 🚀 Quick Start

Clone this repo and follow the tool setup:

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name/
```

---



