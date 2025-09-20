
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

<img width="796" height="599" alt="Image" src="https://github.com/user-attachments/assets/11334b1d-1ab6-4a74-9613-bb937953e652" />

✅ yosys Installation Done

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

<img width="619" height="621" alt="Image" src="https://github.com/user-attachments/assets/3a7964e0-b644-4481-a0b5-a7f415353260" />

✅ Gtkwave Installation Done
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

<img width="619" height="593" alt="Image" src="https://github.com/user-attachments/assets/e36d67a9-ccc6-4634-a752-04511d16b4cf" />

✅ Magic Installation Done
---

## 🚶 Step 7. Openlane Tool Installtion

```bash
$ sudo groupadd docker
$ sudo usermod -aG docker $USER
$ sudo reboot # REBOOT!
$ git clone --depth 1 https://github.com/The-OpenROAD-Project/OpenLane.git
cd OpenLane/
$ make
$ make test # This a ~5 minute test that verifies that the flow and the pdk were properly installed
## test gtkwave
$ gtkwave
```
---
## ⚙️ Openlane Tool Verification

<img width="945" height="260" alt="Image" src="https://github.com/user-attachments/assets/057450a9-a599-4922-bbe3-86aaa68c62ed" />

## Make command run 
<img width="1007" height="491" alt="Image" src="https://github.com/user-attachments/assets/8c76fa4c-fe9e-445f-9638-4cb9aad5de58" />

## make Test Run

<img width="1002" height="626" alt="Image" src="https://github.com/user-attachments/assets/56c05bdc-64fb-413b-a656-042e28995494" />

## Error in Make due to Sky PDK Version 

<img width="645" height="78" alt="Image" src="https://github.com/user-attachments/assets/fdf6192a-fc7b-4c50-a95d-3a9e97df775f" />

## Need committ changes in Makefile version 

<img width="744" height="109" alt="Image" src="https://github.com/user-attachments/assets/5e23129c-e0b4-45db-920f-31f66e863f18" />



✅ Openlane Installation Done


## 🚶🚶🚶 Tools Final Summary

| Tool        | Status     | Primary Use          |
|-------------|------------|---------------------|
|1.  **Yosys**      | ✅ Complete | For RTL Synthesis       |
|2.   **Iverilog**   | ✅ Complete | For Verilog Simulation  |
|3.   **GTKWave**    | ✅ Complete | For Waveform Viewing    |
|4.   **Ngspice**    | ✅ Complete | For Circuit Simulation  |
|5.   **Magic VLSI** | ✅ Complete | For Layout Design       |
|6.   **OpenLane**   | ✅ Complete | For RTL-to-GDS flow     |
---

🏆 Finished Week -0 Assignemtn for Building EDA tool Environment


