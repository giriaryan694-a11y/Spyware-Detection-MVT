# Spyware-Detection-MVT

**Automated detection of mobile spyware and zero-click attacks using MVT and AI-researched IOCs.**

![MVT](https://img.shields.io/badge/MVT-Tool-blue) ![Python](https://img.shields.io/badge/Python-3.8%2B-yellow)

---

## 🔹 Overview

This repository leverages the **Mobile Verification Toolkit (MVT)** to detect traces of government-grade spyware such as Pegasus, Predator, Reign, and FinFisher on **iOS and Android backups**.  

The **STIX2 IOCs** used for detection are compiled from **real-world spyware cases** analyzed by AI research.

---

## 🔹 Features

- Detects spyware artifacts from **iOS & Android backups**.
- Identifies **zero-click exploits** including Pegasus and Predator.
- Works offline, ensuring safety and privacy.
- Provides detailed reports of detected IOCs and suspicious files.

---

## 🔹 Installation

### **Linux / macOS**
```bash
git clone https://github.com/giriaryan694-a11y/Spyware-Detection-MVT.git
cd Spyware-Detection-MVT
python3 -m venv mvt-env
source mvt-env/bin/activate
pip install -r requirements.txt
```
### **Windows**
```
git clone https://github.com/giriaryan694-a11y/Spyware-Detection-MVT.git
cd Spyware-Detection-MVT
python -m venv mvt-env
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass  ## To avoid blocking from windows defender it will work only for current powersell session
.\mvt-env\Scripts\Activate.ps1
pip install -r requirements.txt
```
## 🔹 Usage
### iOS Backup Analysis
```
mvt-ios check-backup --iocs Spyware-Detection-MVT.stix2 /path/to/backup
```
### Android Backup Analysis
```
mvt-android check-backup --iocs Spyware-Detection-MVT.stix2 backup.ab
```
### Direct Device Check (iOS)
```
mvt-ios check-device --iocs Spyware-Detection-MVT.stix2
```
MVT generates a report highlighting all suspicious artifacts found in the backup

## 🔹 Supported Spywares / Zero-Click Exploits
> Pegasus (NSO Group) – iOS & Android, multiple zero-click exploits.
> Predator (Cytrox) – SMS/email zero-click attacks.
> Reign / QuaDream – Android & iOS implants.
> FinFisher / Hacking Team – targeted spyware.
> ⚠️ Note: MVT primarily detects traces from backups. Active implants may not always be detected in real-time.

## 🔹 Disclaimer
> This tool is for educational and defensive research purposes only.
> Always backup devices safely before performing any scans.
> The IOCs were compiled from AI-driven research of real-world spyware cases.

## 🔹 References
> https://github.com/mvt-project/mvt
> AI-driven research for STIX2 IOCs.
