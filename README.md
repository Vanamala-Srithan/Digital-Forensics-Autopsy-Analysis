\# Digital Forensics and Analysis with Autopsy



A practical digital forensics project based on a TryHackMe disk-analysis challenge using \*\*Autopsy\*\* to investigate a forensic disk image, recover digital artifacts, analyze user activity, and identify evidence from a Windows system.



\---



\## 📌 Project Overview



This project demonstrates the practical application of \*\*Digital Forensics and Incident Analysis\*\* using the \*\*Autopsy Forensic Browser\*\*.



The investigation was performed using a forensic disk image provided through a TryHackMe challenge. The objective was to examine the evidence without directly interacting with the original system and recover information related to:



\* System information

\* User accounts

\* User activity

\* Network configuration

\* Browser artifacts

\* PowerShell history

\* Downloaded files

\* Recently accessed documents

\* Application information

\* YARA-related artifacts

\* Exploit-related files

\* File and system metadata



The project provided hands-on experience with a structured forensic investigation workflow and artifact-based evidence analysis.



\---



\## 🎯 Objectives



The main objectives of this project were to:



\* Understand the fundamentals of digital forensics.

\* Learn the workflow of forensic disk-image analysis.

\* Use Autopsy for forensic investigation.

\* Examine Windows system artifacts.

\* Identify user accounts and activity.

\* Analyze network-related information.

\* Investigate browser artifacts.

\* Examine PowerShell command history.

\* Analyze downloaded and recently accessed files.

\* Use keyword searching to locate specific artifacts.

\* Recover information required to solve forensic CTF questions.

\* Document forensic findings and investigation results.



\---



\## 🛠️ Tools and Technologies



| Tool / Platform    | Purpose                                                |

| ------------------ | ------------------------------------------------------ |

| \*\*Autopsy\*\*        | Digital forensic investigation and disk-image analysis |

| \*\*The Sleuth Kit\*\* | Underlying forensic framework used by Autopsy          |

| \*\*TryHackMe\*\*      | Hands-on digital forensics challenge environment       |

| \*\*Windows\*\*        | Operating system represented in the forensic image     |

| \*\*Web Browser\*\*    | Accessing the TryHackMe investigation environment      |



\---



\## 🏗️ Investigation Workflow



```text

&#x20;                TryHackMe

&#x20;                    │

&#x20;                    ▼

&#x20;         Digital Forensics Lab

&#x20;                    │

&#x20;                    ▼

&#x20;            Forensic Evidence

&#x20;               Disk Image

&#x20;                    │

&#x20;                    ▼

&#x20;                Autopsy

&#x20;                    │

&#x20;       ┌────────────┼─────────────┐

&#x20;       ▼            ▼             ▼

&#x20;  System Data   User Activity   File System

&#x20;       │            │             │

&#x20;       ▼            ▼             ▼

&#x20;  OS / Network   Users / Logs   Files / Metadata

&#x20;       │            │             │

&#x20;       └────────────┼─────────────┘

&#x20;                    ▼

&#x20;             Artifact Analysis

&#x20;                    │

&#x20;                    ▼

&#x20;            Evidence Recovery

&#x20;                    │

&#x20;                    ▼

&#x20;            CTF Question Answers

&#x20;                    │

&#x20;                    ▼

&#x20;             Final Findings

```



\---



\# 🔎 Investigation Process



\## 1. Accessing the TryHackMe Lab



The investigation was performed using the TryHackMe digital forensics environment.



The required forensic lab machine was started and the provided investigation environment was accessed.



\### Tasks Performed



\* Logged into TryHackMe.

\* Opened the Digital Forensics / Disk Analysis and Autopsy challenge.

\* Started the provided lab machine.

\* Accessed the forensic investigation environment.



\---



\## 2. Opening the Case in Autopsy



Autopsy was launched to begin the forensic investigation.



The provided case file was opened through:



```text

Autopsy

&#x20;  ↓

Open Case

&#x20;  ↓

Case Files

&#x20;  ↓

TryHackMe Case

```



The required forensic evidence image was then loaded into the case.



\---



\## 3. Loading the Forensic Image



The missing evidence image was located from the provided files directory and added to the Autopsy case.



The evidence was then processed by Autopsy to make its forensic artifacts available for investigation.



The forensic image used an \*\*E01\*\* evidence format.



\---



\# 🧪 Case Analysis



\## 4. Evidence Hash Analysis



The MD5 hash associated with the E01 forensic image was examined.



Hash values are important in digital forensics because they can be used to verify the integrity and identity of forensic evidence.



\### Evidence Examined



\* E01 forensic image

\* MD5 hash



\### Technique



\*\*Hash Verification / Evidence Integrity Analysis\*\*



\---



\## 5. Operating System Information



The operating system information available within the forensic image was examined.



This included identifying system-related information such as:



\* Computer account information

\* Operating system details

\* System configuration



\### Technique



\*\*Operating System Artifact Analysis\*\*



\---



\## 6. User Account Analysis



The user-related artifacts within the forensic image were examined.



The investigation identified multiple user accounts and analyzed available information associated with those accounts.



\### Evidence Examined



\* User profiles

\* User account information

\* User activity

\* Access information



\### Technique



\*\*User Profile Analysis\*\*



\---



\## 7. Last Logged-in User



User activity and access information were examined to identify the user who most recently accessed the system.



This was determined by analyzing the available user-related timestamps and artifacts.



\### Technique



\*\*User Activity and Timeline Analysis\*\*



\---



\## 8. Network Information



The forensic image was examined for network-related information.



The investigation identified:



\* Computer IP address

\* Network adapter information

\* Network-related software



The installed network monitoring application \*\*Look@LAN\*\* was also identified during the investigation.



\### Techniques



\* Network Artifact Analysis

\* Installed Software Analysis

\* System Information Analysis



\---



\## 9. Browser Bookmark Analysis



Browser artifacts were examined using Autopsy.



The investigation identified a saved \*\*Google Maps\*\* bookmark associated with the user.



\### Evidence Examined



\* Browser bookmarks

\* Saved URLs

\* User browsing artifacts



\### Technique



\*\*Browser Artifact Analysis\*\*



\---



\## 10. Desktop Wallpaper Analysis



The forensic image contained image-related evidence associated with the user's desktop.



The desktop wallpaper was examined to identify the full name displayed in the image.



\### Technique



\*\*Image Artifact Analysis\*\*



\---



\## 11. PowerShell History Analysis



PowerShell command history was examined to identify previously executed commands.



The investigation navigated through the user's profile and examined the PowerShell history stored under the user's application data.



Relevant path:



```text

Users

└── <User>

&#x20;   └── AppData

&#x20;       └── Roaming

&#x20;           └── Microsoft

&#x20;               └── Windows

&#x20;                   └── PowerShell

&#x20;                       └── PSReadLine

```



The PowerShell console history contained commands that helped recover one of the challenge flags.



\### Evidence Examined



\* PowerShell history

\* Console commands

\* User activity



\### Technique



\*\*Command History Analysis\*\*



\---



\## 12. Desktop File Analysis



The user's Desktop directory was examined for suspicious or relevant files.



The investigation identified a text/exploit-related file containing information required for the challenge.



\### Evidence Examined



\* Desktop files

\* Text files

\* Exploit-related artifacts



\### Technique



\*\*File System Analysis\*\*



\---



\## 13. Downloaded Password Tools



The user's Downloads directory was investigated.



Two password-focused tools were identified within the downloaded files.



The investigation also examined \*\*Prefetch artifacts\*\* to obtain additional information related to application execution.



\### Evidence Examined



\* Downloads directory

\* Executable files

\* Prefetch artifacts



\### Techniques



\* File System Analysis

\* Application Analysis

\* Prefetch Analysis



\---



\## 14. YARA File Investigation



A keyword search was performed in Autopsy to locate YARA-related artifacts.



The keyword used during the investigation was:



```text

yar

```



The search identified a YARA-related file within the forensic image.



The file was examined to identify associated metadata, including the author information.



\### Techniques



\* Keyword Search

\* File Metadata Analysis

\* Artifact Identification



\---



\## 15. Recent Documents Analysis



The Recent Documents artifacts were examined to identify suspicious or recently accessed files.



The investigation navigated through the user's application data and Windows Recent Items.



Relevant path:



```text

Users

└── <User>

&#x20;   └── AppData

&#x20;       └── Roaming

&#x20;           └── Microsoft

&#x20;               └── Windows

&#x20;                   └── Recent

```



An exploit-related document was identified from the recently accessed files.



\### Technique



\*\*Recent File / User Activity Analysis\*\*



\---



\# 📂 Recovered Artifacts



The investigation successfully identified and analyzed multiple categories of digital evidence.



| Artifact Category   | Evidence Recovered                     |

| ------------------- | -------------------------------------- |

| System Information  | Computer account and OS information    |

| User Information    | User accounts and activity             |

| Login Activity      | Last accessed user                     |

| Network Information | IP address and network adapter         |

| Network Software    | Look@LAN                               |

| Browser Data        | Google Maps bookmark                   |

| Image Evidence      | Desktop wallpaper information          |

| PowerShell          | Console command history                |

| Desktop Files       | Text and exploit-related files         |

| Downloads           | Password-focused tools                 |

| Prefetch            | Application execution artifacts        |

| YARA                | YARA-related file and metadata         |

| Recent Documents    | Recently accessed exploit-related file |

| Evidence Metadata   | MD5 hash of forensic image             |



\---



\# 🧰 Forensic Techniques Used



The following techniques were used during the investigation:



\### 1. Disk Image Analysis



Analyzed the provided E01 forensic image using Autopsy.



\### 2. Hash Analysis



Examined the MD5 hash associated with the forensic image.



\### 3. File System Analysis



Inspected directories, files, and user profiles.



\### 4. Metadata Analysis



Examined available file and system metadata.



\### 5. User Activity Analysis



Investigated user accounts and activity-related artifacts.



\### 6. Browser Artifact Analysis



Examined browser bookmarks and saved browsing information.



\### 7. PowerShell History Analysis



Recovered previously executed PowerShell commands.



\### 8. Prefetch Analysis



Used Windows Prefetch artifacts to identify application-related activity.



\### 9. Keyword Searching



Used Autopsy's keyword search functionality to locate specific artifacts.



\### 10. Recent File Analysis



Examined recently accessed documents and Windows Recent Items.



\---



\# 🚩 CTF Investigation Questions



The TryHackMe challenge contained multiple forensic questions requiring the investigator to locate specific information within the forensic image.



The questions involved identifying information such as:



\* MD5 hash of the E01 image

\* Computer account name

\* User accounts

\* Last logged-in user

\* Computer IP address

\* Network adapter

\* Network monitoring tool

\* Google Maps bookmark

\* Full name displayed on the desktop wallpaper

\* PowerShell-related flag

\* Desktop file flag

\* Password-focused tools

\* YARA file author

\* Exploit name



All required questions were investigated and successfully completed.



> \*\*Note:\*\* Challenge-specific flags and answers are intentionally not published in this README. The screenshots and final project report contain the evidence collected during the investigation.



\---



\# 📸 Screenshots



Screenshots documenting the investigation are stored in the `screenshots/` directory.



Suggested screenshot organization:



```text

screenshots/

│

├── 01-tryhackme-lab.png

├── 02-autopsy-case.png

├── 03-evidence-image.png

├── 04-md5-hash.png

├── 05-system-information.png

├── 06-user-accounts.png

├── 07-browser-bookmark.png

├── 08-powershell-history.png

├── 09-password-tools.png

├── 10-yara-search.png

├── 11-recent-documents.png

└── 12-room-completed.png

```



\---



\# 📄 Project Report



The complete investigation report contains:



\* Project introduction

\* Lab setup

\* Case analysis

\* Investigation methodology

\* Recovered artifacts

\* Key findings

\* CTF investigation results

\* Screenshots

\* Challenges encountered

\* Conclusions

\* References



The final report is available in:



```text

report/

└── Digital-Forensics-Autopsy-Report.pdf

```



\---



\# 🔐 Evidence Handling



The project follows a basic forensic evidence-handling approach.



The original forensic image was analyzed within the provided investigation environment rather than modifying the original evidence directly.



Hash information was also examined as part of the evidence verification process.



For privacy, security, and repository-size considerations, the original E01 forensic image is \*\*not included in this repository\*\*.



\---



\# ⚠️ Disclaimer



This project was performed in an authorized educational environment provided by TryHackMe.



All forensic analysis was conducted for educational and cybersecurity training purposes.



The tools and techniques demonstrated in this project should only be used on systems and digital evidence for which proper authorization has been obtained.



\---



\# 🎓 Skills Demonstrated



This project demonstrates practical exposure to:



\* Digital Forensics

\* Computer Forensics

\* Disk Image Analysis

\* Autopsy

\* The Sleuth Kit

\* Evidence Analysis

\* File System Analysis

\* Metadata Analysis

\* User Activity Investigation

\* Windows Forensics

\* Browser Forensics

\* PowerShell Forensics

\* Prefetch Analysis

\* Keyword Searching

\* Artifact Recovery

\* Incident Investigation

\* CTF-Based Investigation

\* Technical Documentation



\---



\# 📚 Learning Outcomes



After completing this project, I gained practical experience in:



1\. Understanding the digital forensic investigation process.

2\. Working with forensic disk images.

3\. Using Autopsy for evidence analysis.

4\. Investigating Windows user activity.

5\. Extracting system and network information.

6\. Analyzing browser artifacts.

7\. Recovering PowerShell command history.

8\. Investigating suspicious files and downloaded tools.

9\. Using Prefetch artifacts for application analysis.

10\. Locating evidence through keyword searches.

11\. Examining recently accessed documents.

12\. Documenting forensic findings in a structured format.



\---



\# 🚀 Future Improvements



Potential improvements to this project include:



\* Performing timeline analysis using additional forensic artifacts.

\* Investigating Windows Registry artifacts in greater depth.

\* Analyzing deleted files and file recovery.

\* Performing browser history and cache analysis.

\* Creating a detailed forensic timeline.

\* Investigating additional Windows event logs.

\* Performing memory forensics using tools such as Volatility.

\* Integrating additional forensic tools for cross-validation.

\* Creating automated forensic artifact collection workflows.



\---



\# 📖 References



\* \[TryHackMe](https://tryhackme.com/)

\* \[Autopsy](https://www.autopsy.com/)

\* \[Autopsy Documentation](https://www.autopsy.com/documentation/)

\* \[The Sleuth Kit](https://www.sleuthkit.org/)



\---



\## 👨‍💻 Project Information



\*\*Project:\*\* Digital Forensics and Analysis with Autopsy



\*\*Domain:\*\* Cyber Security / Digital Forensics



\*\*Platform:\*\* TryHackMe



\*\*Primary Tool:\*\* Autopsy



\*\*Evidence Type:\*\* Forensic Disk Image (E01)



\*\*Investigation Type:\*\* Disk and Artifact Analysis



\*\*Project Status:\*\* Completed



