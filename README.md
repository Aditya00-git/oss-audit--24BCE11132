# OSS Capstone Audit — Git

This is my submission for the Open Source Audit capstone project done as part of the Open Source Software course at VITyarthi.

I picked Git for this audit because its literally everywhere. Every project, every internship, every dev job — Git is the first thing they ask if you know. So it made sense to actually dig into it properly rather than just use it blindly.

---

**Name:** Aditya Seswani  
**Reg No:** 24BCE11132  
**Course:** Open Source Software (NGMC) — VITyarthi  
**Software Audited:** Git (GPL v2)  

---

## About the Project

The main idea was to understand Git not just as a tool but as an open source project — where it came from, why it was made free, and what that means in the bigger picture of software development.

Some things I covered in the report:
- How Git was born after BitKeeper pulled its free license from the Linux community
- What GPL v2 actually means and how it protects user freedom
- How Git lives and works inside a Linux system
- Why open source matters and how it compares to proprietary software
- Then 5 shell scripts to put the Linux stuff into practice

---

## Repo Structure

```
oss-audit-24BCE11132/
├── README.md
├── Screenshot/
├── OSSCapstoneProject.pdf
├── script1_system_identity.sh
├── script2_package_inspector.sh
├── script3_disk_permission_auditor.sh
├── script4_log_analyzer.sh
└── script5_manifesto_generator.sh
```

---

## The Scripts

**Script 1 — System Identity Report**  
Basically prints out info about the system — OS, kernel, current user, uptime, date. Nothing fancy but good practice with variables and command substitution.

**Script 2 — FOSS Package Inspector**  
Checks if Git is installed, figures out whether you're on a Debian or RPM system, and shows package details. Also has a case statement that prints a note about different FOSS tools.

**Script 3 — Disk and Permission Auditor**  
Loops through some standard Linux directories and shows permissions, owner, size etc. Also checks Git specific paths. Helped me understand how Linux handles file permissions better.

**Script 4 — Log File Analyzer**  
You pass a log file path and a keyword, and it counts how many lines match and shows the last 5. Has some retry logic too if the file path doesn't exist. This one took me the most time to get right.

**Script 5 — Manifesto Generator**  
Asks you 3 questions and builds a personalised open source philosophy statement from your answers. Saves it to a txt file. Honestly this one was kind of fun to make.

---

## How to Run

```bash
# clone the repo
git clone https://github.com/Aditya00-git/oss-audit--24BCE11132
cd oss-audit-24BCE11132

# make scripts executable
chmod +x script1_system_identity.sh script2_package_inspector.sh script3_disk_permission_auditor.sh script4_log_analyzer.sh script5_manifesto_generator.sh

# run them
./script1_system_identity.sh
./script2_package_inspector.sh
./script3_disk_permission_auditor.sh
./script4_log_analyzer.sh /var/log/syslog error
./script5_manifesto_generator.sh
```

You need a Linux system with bash and Git installed. Thats pretty much it, no extra dependencies.

---

## About Git

Git was created by Linus Torvalds in 2005. Its a distributed version control system licensed under GPL v2. The current maintainer is Junio C Hamano. Official site is git-scm.com.

---

## Note

All scripts were written by me and tested on Linux. The report and code are my own work submitted for the VITyarthi OSS capstone.
