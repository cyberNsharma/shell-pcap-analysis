# 🐚 Shell PCAP Analysis

This repository contains the analysis of the `shell.pcap` file.  
The PCAP captures multiple reverse shells and related activities. This repo is designed for learning, reference, and cyber forensics practice.

---

## 📂 Repository Contents

| File | Description |
|------|-------------|
| `Q1.md` | Detailed analysis of the first shell (port, commands executed) |
| `Q2.md` | Detailed analysis of the second shell (port, file added) |
| `Q3.md` | Analysis of file transfers within the PCAP |
| `filters.md` | List of Wireshark filters used in the analysis |
| `tools.md` | Tools & commands used (Wireshark, tshark, Linux CLI, etc.) |
| `summary.md` | Consolidated findings and key takeaways from the analysis |

---

## ⚙️ Platforms & Tools

- **Wireshark** – GUI packet analysis  
- **Tshark** – CLI packet analysis  
- **Linux Terminal** – Commands like `strings`, `grep`, `cat`  
- **Python (optional)** – For parsing PCAPs programmatically  

---

## 📝 Analysis Performed

- Identified reverse shells and their listening ports.  
- Followed TCP streams to observe commands and file transfers.  
- Extracted file contents (e.g., `/etc/passwd`) from network streams.  
- Applied filters to isolate specific sessions and suspicious activity.  

---

## 🔍 Filters Used (Examples)

- Filter for first shell:  
  ```wireshark
  tcp.port == 4444
   http and many more filters and steps check in analysis file.
