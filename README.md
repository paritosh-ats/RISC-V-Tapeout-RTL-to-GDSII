# 🚀 RISC-V Tapeout Program — Day 0

This repository documents my **Day 0** progress for the RISC-V Tapeout Program by VLSI System Design (VSD). The goal is to set up a complete environment with essential tools for RISC-V SoC design and verification.

---

## 📌 Tasks Overview

### 1️⃣ Install Oracle Virtual Machine
- Download **Oracle VirtualBox** from the official site.
- Install it on a Windows machine to create a Linux virtual environment.

![Oracle VM Installation](images/oracle_vm_installed.png)

---

### 2️⃣ Set Up Ubuntu on VirtualBox
- Download the latest **Ubuntu ISO** image.
- Create and configure a new VM in VirtualBox.
- Mount and install Ubuntu using the ISO.
- Complete Ubuntu setup and updates *(this may take a while)*.

![Ubuntu Installation](images/ubuntu_installation.png)
![Ubuntu Running](images/ubuntu_running.png)

---

### 3️⃣ Install and Verify Required Tools

#### 🔷 Yosys — Logic Synthesis Framework
```bash
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make
sudo apt-get install build-essential clang bison flex libreadline-dev \
gawk tcl-dev libffi-dev git graphviz xdot pkg-config python3 \
libboost-system-dev libboost-python-dev libboost-filesystem-dev zlib1g-dev
make config-gcc
make
sudo make install
```
![Yosys Installation](images/yosys_installation.png)

---

#### 🔷 Icarus Verilog (Iverilog) — Verilog Simulator
```bash
sudo apt-get update
sudo apt-get install iverilog
```
![Iverilog Installed](images/iverilog_installed.png)

---

#### 🔷 GTKWave — Waveform Viewer
```bash
sudo apt update
sudo apt install gtkwave
```
![GTKWave Installed](images/gtkwave_installed.png)

---

#### 🔷 Ngspice — Mixed-Signal Circuit Simulator
```bash
sudo apt update
sudo apt install ngspice
```
![Ngspice Installed](images/ngspice_installed.png)

---

#### 🔷 Magic VLSI — IC Layout Tool
```bash
sudo apt-get install m4 tcsh csh libx11-dev tcl-dev tk-dev \
libcairo2-dev mesa-common-dev libglu1-mesa-dev libncurses-dev
git clone https://github.com/RTimothyEdwards/magic
cd magic
./configure
make
sudo make install
```
![Magic VLSI Installed](images/magic_vlsi_installed.png)

---

## ✅ Outcome
All required tools and the Ubuntu environment have been successfully set up, providing a solid foundation for upcoming RISC-V SoC design and tape-out tasks.
