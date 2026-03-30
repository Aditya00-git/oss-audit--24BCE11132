# Open Source Software Audit — Git (Distributed Version Control System)

**Course:** Open Source Software (NGMC) — VITyarthi  
**Student:** Aditya Seswani  
**Roll Number:** 24BCE11132  
**Audited Software:** Git | License: GNU GPL v2  

---

## Why Git?

Git was chosen for this audit because it represents one of the most impactful pieces of
open-source infrastructure ever built. Created by Linus Torvalds in April 2005 after
the Linux kernel community lost access to BitKeeper (a proprietary VCS), Git was built
out of necessity — and released freely so that history would never repeat itself.

Today, Git underpins billions of dollars worth of software projects worldwide, yet remains
free, open, and community-maintained. That story sits at the heart of what this course is about.

---

## What This Repository Contains

```
oss-audit-24BCE11132/
│
├── README.md                            ← You are here
├── Screenshot/                          ← Script execution screenshots
├── OSSCapstoneProject.pdf               ← Overall report
├── script1_system_identity.sh           ← Prints system and OS info
├── script2_package_inspector.sh         ← Inspects Git installation details
├── script3_disk_permission_auditor.sh   ← Audits directories and permissions
├── script4_log_analyzer.sh              ← Parses and analyzes log files
└── script5_manifesto_generator.sh       ← Generates a personal OSS statement
```

---

## Script Breakdown

### Script 1 — System Identity Report
Gathers and displays core system information in a formatted layout.
Output includes: OS name, kernel version, current user, home directory,
system uptime, and current date/time. Closes with a note about the GPL v2
license that governs the Linux kernel itself.

Key concepts practiced: `uname`, `whoami`, `uptime`, `date`, `lsb_release`,
command substitution `$()`, and variable use with `echo`.

---

### Script 2 — FOSS Package Inspector
Detects whether Git is installed, identifies the system's package manager
(RPM-based or Debian-based), and retrieves version and license metadata.
Uses a `case` statement to display a brief FOSS philosophy note for
several well-known open-source tools.

Key concepts practiced: `if-then-else`, `case` statement, `command -v`,
`rpm -qi`, `dpkg -l`, pipes with `grep`.

---

### Script 3 — Disk and Permission Auditor
Iterates over a set of standard Linux directories (`/etc`, `/var/log`, `/home`,
`/usr/bin`, `/tmp`) as well as Git-specific paths. Reports the size, permission
bits, owner, and group for each location. Also locates the Git binary and
reports on it separately.

Key concepts practiced: `for` loop with arrays, `if [ -d ]`, `ls -ld`, `awk`,
`du -sh`, `cut`.

---

### Script 4 — Log File Analyzer
Takes a log file path as a required argument and an optional keyword (defaults
to `error`). Reads through the file line by line, counts how many lines match
the keyword, and prints the five most recent matching lines. Includes retry
logic to look for alternative log files if the given path does not exist.

Key concepts practiced: `while IFS= read -r`, argument handling with `$1`/`$2`,
`${var:-default}`, counter variables, `grep -i`, `tail`, retry loops.

---

### Script 5 — Open Source Manifesto Generator
An interactive script that prompts the user with three questions and uses the
answers to generate a customised open-source philosophy statement. The output
is saved to a `.txt` file named after the current user and also printed to screen.

Key concepts practiced: `read -p`, input validation with `while [ -z ]`,
string concatenation, file output with `>` and `>>`, `date`, `cat`, `whoami`.

---

## Running the Scripts

### Prerequisites
- Any mainstream Linux distribution (Ubuntu, Debian, Fedora, Arch, etc.)
- Bash shell — verify with `bash --version`
- Git installed — `sudo apt install git` or `sudo dnf install git`

### Setup

```bash
# Step 1: Clone the repository
git clone https://github.com/Aditya00-git/oss-audit--24BCE11132
cd oss-audit-24BCE11132

# Step 2: Grant execute permissions
chmod +x script1_system_identity.sh script2_package_inspector.sh \
         script3_disk_permission_auditor.sh script4_log_analyzer.sh \
         script5_manifesto_generator.sh
```

### Execution

```bash
# Script 1 — no arguments needed
./script1_system_identity.sh

# Script 2 — no arguments needed
./script2_package_inspector.sh

# Script 3 — no arguments needed
./script3_disk_permission_auditor.sh

# Script 4 — log path required, keyword optional
./script4_log_analyzer.sh /var/log/syslog            # uses default keyword 'error'
./script4_log_analyzer.sh /var/log/syslog warning    # custom keyword
./script4_log_analyzer.sh /var/log/messages error    # for RHEL/CentOS systems

# Script 5 — interactive, no arguments needed
./script5_manifesto_generator.sh
# Output saved to: manifesto_<yourusername>.txt
```

---

## Tool Dependencies

| Script | Tools Used |
|--------|-----------|
| Script 1 | `uname`, `whoami`, `uptime`, `date`, `lsb_release` |
| Script 2 | `rpm` or `dpkg`, `git`, `grep` |
| Script 3 | `ls`, `du`, `awk`, `cut`, `which` |
| Script 4 | `grep`, `tail` |
| Script 5 | `date`, `cat`, `whoami` |

All tools listed above come pre-installed on standard Linux distributions.
No third-party packages are required.

---

## Git — Quick Reference

| Field | Value |
|-------|-------|
| Type | Distributed Version Control System |
| Creator | Linus Torvalds |
| First Released | April 2005 |
| Current Maintainer | Junio C Hamano |
| License | GNU General Public License v2 (GPL v2) |
| Official Website | https://git-scm.com |
| Source Code | https://github.com/git/git |

---

## Submission Note

This repository is submitted as the OSS Capstone Project for the VITyarthi
Open Source Software course. It is accompanied by a project report (PDF) that
covers the origin story of Git, a GPL v2 license analysis, Git's Linux footprint,
and a broader discussion of the FOSS ecosystem.

