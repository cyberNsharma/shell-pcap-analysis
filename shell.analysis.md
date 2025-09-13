# 📝 Shell PCAP Analysis Notes

This file contains all questions, answers, and Wireshark filters used during the `shell.pcap` analysis in a single, structured format.

---

**Q1: What port is the shell listening on?**  
**Answer:** 4444  

**Q2: What is the port for the second shell?**  
**Answer:** 9999  

**Q3: What version of netcat is installed?**  
**Answer:** 1.10-41.1  

**Q4: What file is added to the second shell?**  
**Answer:** /etc/passwd  

**Q5: What password is used to elevate the shell?**  
**Answer:** *umR@Q%4V&RC  

**Q6: What is the codename of the target system's OS version?**  
**Answer:** bionic  

**Q7: How many users are on the target system?**  
**Answer:** 31  

---

**Filter used:**  
```wireshark
tcp.port == 4444 || tcp.port == 9999
tcp.port > 1024 && !(tcp.port == 4444 || tcp.port == 9999)
tcp.stream eq <stream_number_of_shell>
tcp.stream eq <stream_number_with_os_info>
