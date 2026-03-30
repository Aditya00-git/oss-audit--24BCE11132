# OSS Capstone Audit — Git

This repository contains my submission for the Open Source Audit capstone project for the Open Source Software course (VITyarthi).

The project focuses on Git, a distributed version control system created by Linus Torvalds in 2005 and licensed under the GNU General Public License v2 (GPL v2).

--------------------------------------------------

Student Details

Name: Aditya Seswani  
Registration Number: 24BCE11132  
Course: Open Source Software (NGMC)  
Software Audited: Git  

--------------------------------------------------

About the Project

This project explores Git from both a technical and philosophical perspective.

It includes:
- Study of Git’s origin and purpose  
- Understanding of its GPL v2 license  
- Ethical discussion of open-source software  
- Analysis of how Git exists in a Linux system  
- Comparison with proprietary alternatives  
- Practical implementation using shell scripts  

--------------------------------------------------

Repository Structure

oss-audit-24BCE11132/

├── Screenshot

├── README.md

├── script1_system_identity.sh

├── script2_package_inspector.sh

├── script3_disk_permission_auditor.sh

├── script4_log_analyzer.sh

└── script5_manifesto_generator.sh

--------------------------------------------------

Shell Scripts Overview

Script 1 — System Identity Report  
Displays system details like OS name, kernel version, user, uptime, and date.

Script 2 — FOSS Package Inspector  
Checks if Git is installed and shows package details.

Script 3 — Disk and Permission Auditor  
Analyzes system directories and displays size, permissions, owner, and group.

Script 4 — Log File Analyzer  
Reads a log file, counts keyword occurrences, and displays results.

Script 5 — Open Source Manifesto Generator  
Takes user input and generates a personalized open-source statement.

--------------------------------------------------

How to Run the Scripts

1. Clone the repository
git clone https://github.com/Aditya00-git/oss-audit--24BCE11132
cd oss-audit-24BCE11132

2. Give execution permission
chmod +x script1_system_identity.sh
chmod +x script2_package_inspector.sh
chmod +x script3_disk_permission_auditor.sh
chmod +x script4_log_analyzer.sh
chmod +x script5_manifesto_generator.sh

3. Run scripts
./script1_system_identity.sh
./script2_package_inspector.sh
./script3_disk_permission_auditor.sh
./script4_log_analyzer.sh /var/log/syslog error
./script5_manifesto_generator.sh

--------------------------------------------------

Requirements

- Linux system (Ubuntu, Debian, Fedora, etc.)
- Bash shell
- Git installed

--------------------------------------------------

About Git

Type: Version Control System  
Created by: Linus Torvalds  
License: GPL v2  
Purpose: Track changes in code and enable collaboration  

--------------------------------------------------

Note

All scripts were tested on a Linux environment and executed through the terminal.

--------------------------------------------------

Submission

This repository is part of the OSS Capstone Project submission and is accompanied by a report PDF.
