
##  🚀 Week 0: OpenEDA Tool Setup within VirtualBox-Ubuntu
## 🖥️ Virtual Machine Configuration requirement (Ubuntu 20.04+)

| Resource   | Allocation     | Remarks                                |
|------------|----------------|----------------------------------------|
| 💾 RAM     | 6 GB           | Sufficient for running EDA tools smoothly |
| 📀 Storage | 50 GB HDD      | Enough space for OS + tools + projects |
| 🧮 CPU     | 4 vCPUs        | Provides parallelism for synthesis & PnR |
| 🐧 OS      | Ubuntu 20.04+  | Recommended version for open-source EDA tools |

## ⚙️ Tool Installation
- 👉 Copy the below commands and execute on ubuntu terminal.

## 🚶 Step 1. Git installation 
```bash
$ git --version
$ sudo apt install git # (If git reports no version. please install it) 
```

## 🚶 Step 2. Create a Folder VSD using `mkdir`

```bash
$ mkdir vsd  # will create a folder in current path
$ cd vsd     # change current directory to vsd folder
```
## 🚶 Step 3. Cloning from Source: `Yosys`
You need a C++ compiler with C++17 support (up-to-date CLANG or GCC is recommended) and some standard tools such as GNU Flex, GNU Bison, and GNU Make. 

## Perfect! Here’s your complete Yosys installation scrip
```bash
$ cd vsd
## clone Yosys
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys
$ git submodule update --init --recursive 
## Dependencies of Yosys
$ sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ git submodule update --init --recursive (if make reports error) 
## make yoysy
$ make config-gcc 
## install yoysy
$ sudo make install
## test yosys
$ yosys (test yosys)
```
---
## ⚙️ Yosys Tool Verification


---
## 🚶 Step 4. iverilog Installtion
```bash
$ 
$ sudo apt-get update
$ sudo apt-get install iverilog
## test iverilog
$ iverilog
```
---
## ⚙️ iverilog Tool Verification


<img width="813" height="395" alt="Image" src="https://github.com/user-attachments/assets/1b149055-c903-447a-b09c-7034795e6481" />

✅ iverilog Installation Done
---

## 🚶 Step 5. Gtkwave Installtion
```bash
$ 
$ sudo apt-get update
$ sudo apt-get install gtkwave
## test gtkwave
$ gtkwave
```
---
## ⚙️ Gtkwave Tool Verification

---
## 🚶 Step 6. Ngspice – Circuit Simulator
```bash

$ sudo apt-get update
$ sudo apt-get install ngspice
## test ngspice 
$ ngspice

```
---
## ⚙️ Ngspice Tool Verification

<img width="624" height="442" alt="Image" src="https://github.com/user-attachments/assets/d52c7288-73c5-4551-9cde-6a67325f0ea9" />

✅ Ngspice Installation Done

---

## 🚶 Step 7. Magic VLSI – Layout Tool
```bash
$ sudo apt-get update
$ sudo apt-get install -y m4 tcsh csh libx11-dev tcl-dev tk-dev \
   libcairo2-dev mesa-common-dev libglu1-mesa-dev libncurses-dev
$ cd vsdflow

# Clone Magic repository
$ git clone https://github.com/RTimothyEdwards/magic
$ cd magic

# Configure build
$ ./configure

# Build Magic
$ make

# Install system-wide
$ sudo make install

# test the installation
$ which magic
$ magic
```
## ⚙️ Magic Tool Verification

---
## 🚶🚶🚶 Tools Final Summary

| Tool        | Status     | Primary Use          |
|-------------|------------|---------------------|
| 🧠 **Yosys**      | ✅ Complete | For RTL Synthesis       |
| 📟 **Iverilog**   | ✅ Complete | For Verilog Simulation  |
| 📊 **GTKWave**    | ✅ Complete | For Waveform Viewing    |
| ⚡ **Ngspice**    | ✅ Complete | For Circuit Simulation  |
| 🎨 **Magic VLSI** | ✅ Complete | For Layout Design       |

---

🏆 Finished Week -0 Assignemtn for Building EDA tool Environment


