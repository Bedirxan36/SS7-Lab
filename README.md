# SigPloit / SigFramework Installation Guide

> Educational SS7/SIGTRAN testing framework  
> Linux • Windows • Termux Installation

---

# Requirements

- Python 3
- Git
- Java 7+
- Internet connection

---

# Linux Installation (Kali / Ubuntu / Debian)

## 1. Update System

```bash
sudo apt update && sudo apt upgrade -y
```

## 2. Install Dependencies

```bash
sudo apt install -y git python3 python3-pip python3-dev \
build-essential default-jdk \
lksctp-tools libsctp-dev wireshark
```

## 3. Enable SCTP

```bash
sudo modprobe sctp
```

## 4. Clone Repository

```bash
git clone https://github.com/SigPloiter/SigPloit.git
```

## 5. Enter Directory

```bash
cd SigPloit
```

## 6. Install Python Requirements

```bash
sudo python3 -m pip install --upgrade pip
sudo python3 -m pip install -r requirements.txt
```

---

# Run SigPloit

```bash
sudo python3 sigploit.py
```

---

# Run SigFramework Web Interface

```bash
cd SigFramework
sudo python3 sigframework_web.py
```

Open browser:

```text
http://127.0.0.1:5000
```

---

# Run GUI

```bash
sudo python3 sigfremwork_gui_main.py
```

---

# Run CLI

```bash
sudo python3 sig_framwork_cli.py
```

---

# Wireshark Filters

## SCTP

```text
sctp
```

## M3UA

```text
m3ua
```

## TCAP

```text
tcap
```

---

# Windows Installation

> WARNING:
> SCTP is not fully supported on Windows.
> Some features may not work correctly.

---

## 1. Install Software

Download and install:

- Python 3
- Git
- Java JDK

---

## 2. Clone Repository

Open CMD or PowerShell:

```powershell
git clone https://github.com/SigPloiter/SigPloit.git
```

---

## 3. Enter Folder

```powershell
cd SigPloit
```

---

## 4. Install Requirements

```powershell
pip install -r requirements.txt
```

---

## 5. Run

```powershell
python sigploit.py
```

---

# Termux Installation (Android)

## 1. Update Packages

```bash
pkg update && pkg upgrade -y
```

---

## 2. Install Dependencies

```bash
pkg install git python clang make -y
```

---

## 3. Install Java

```bash
pkg install openjdk-17 -y
```

---

## 4. Clone Repository

```bash
git clone https://github.com/SigPloiter/SigPloit.git
```

---

## 5. Enter Folder

```bash
cd SigPloit
```

---

## 6. Install Requirements

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

---

# Run on Termux

```bash
python sigploit.py
```

---

# Common Errors

## pysctp Error

Linux only:

```bash
sudo apt install libsctp-dev lksctp-tools
pip install pysctp
```

---

## Permission Denied

```bash
sudo su
```

---

## No module named

```bash
pip install module_name
```

---

# Disclaimer

This project is for:

- Educational purposes
- Authorized testing
- Security research

Unauthorized use against telecom networks is illegal.

---

# Official Repository

https://github.com/SigPloiter/SigPloit
