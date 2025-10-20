# Local Network Port Scan — Task 1

**Author:** RACHANA J 
**Date:** 20/10/2025

## Overview
This repository contains the deliverables for **Task 1: Scan Your Local Network for Open Ports**.  
The objective was to discover open TCP ports on devices in the local network, identify potentially risky services, and recommend remediation steps.

## Files in this repository
- `Local_Network_Port_Scan_Report_Isha_Gowda.docx` — Final report (student-ready Word document).  
- `local_scan_results.txt` — Raw Nmap output from the scan (evidence).  
- `README.md` — This file.


## Summary of findings
- **Network scanned:** `XX.XXX.XX0/24`  
- **Hosts found:**  
  - `XX.XXX.XX.XXX`ort **53/tcp** (DNS) — likely router/DNS resolver (low risk)  
  - `XX.XXX.XX.XXX` — Ports **135/tcp (MSRPC), 139/tcp (NetBIOS-SSN), 445/tcp (Microsoft-DS), 3306/tcp (MySQL)** — medium/high risk depending on configuration

**Notes:** File sharing (SMB/NetBIOS) on the identified host was disabled by the user. MySQL is intentionally in use on the host; hardening recommendations are included in the report.

## How to reproduce the scan
> Only scan networks and devices you own or have explicit permission to test.

1. Install Nmap: https://nmap.org/download.html  
2. Identify your local subnet (Windows example):
   ```powershell
   ipconfig
