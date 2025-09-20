
##  🚀 Week 0: OpenEDA Tool Setup within VirtualBox-Ubuntu
## 🖥️ Virtual Machine Configuration requirement (Ubuntu 20.04+)

| Resource   | Allocation     | Remarks                                |
|------------|----------------|----------------------------------------|
| 💾 RAM     | 6 GB           | Sufficient for running EDA tools smoothly |
| 📀 Storage | 50 GB HDD      | Enough space for OS + tools + projects |
| 🧮 CPU     | 4 vCPUs        | Provides parallelism for synthesis & PnR |
| 🐧 OS      | Ubuntu 20.04+  | Recommended version for open-source EDA tools |

## ⚙️ Tool Installation & Verification 
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
## Perfect! Here’s your complete Yosys installation scrip
```bash
$ cd vsd
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys
$ git submodule update --init --recursive 
$ sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make
$ git submodule update --init --recursive (if make reports error) 
$ make (run make again)
$ sudo make install
$ yosys (test yosys)
```
---
## ⚙️ Tool Installation & Verification
