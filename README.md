**Detailed Notes on Cybersecurity Topics**  
*Prepared by [Newton]*  

---

# 1. Footprinting  
**Definition**: Footprinting is the process of gathering information about a target system or network to identify vulnerabilities and plan attacks. It is the **first phase** of ethical hacking.  

### **Types of Footprinting**  
1. **Passive Footprinting**: Collecting data without direct interaction with the target (e.g., social media, public databases).  
2. **Active Footprinting**: Directly interacting with the target (e.g., DNS queries, network scanning).  

### **Techniques**  
- **DNS Interrogation**: Use `nslookup` or `dig` to extract DNS records (A, MX, NS).  
- **WHOIS Lookup**: Identify domain ownership via WHOIS databases.  
- **Social Engineering**: Extract info from employees via phishing or pretexting.  
- **Website Analysis**: Use tools like **Wappalyzer** to identify tech stacks.  
- **Search Engines**: Google Dorking (`site:`, `filetype:`, `inurl:`).  

### **Tools**  
- **nslookup**/dig: DNS query tools.  
- **theHarvester**: Aggregates emails and subdomains.  
- **Shodan**: Search engine for IoT devices.  
- **Maltego**: Visualizes relationships between data points.  

### **Countermeasures**  
- Restrict DNS zone transfers.  
- Use privacy protection for domain registration.  
- Educate employees about social engineering.  

---

# 2. Network Scanning  
**Definition**: Identifying active devices, open ports, and services on a network to map vulnerabilities.  

### **Objectives**  
- Discover live hosts (e.g., using `ping`).  
- Identify open ports and services (e.g., port 80 for HTTP).  
- Determine OS and device types.  

### **Types of Scanning**  
1. **Port Scanning**:  
   - **TCP SYN Scan**: Half-open scan to avoid detection.  
   - **TCP Connect Scan**: Completes the TCP handshake.  
   - **UDP Scan**: Checks for open UDP ports.  
2. **Network Mapping**: Tools like **Nmap** create network topology diagrams.  
3. **Vulnerability Scanning**: Tools like **Nessus** detect known vulnerabilities.  

### **Tools**  
- **Nmap**: Most popular network scanner (`nmap -sS <IP>`).  
- **Masscan**: Scans the entire internet in minutes.  
- **Wireshark**: Packet analyzer for deep inspection.  

### **Countermeasures**  
- Use firewalls and intrusion detection systems (IDS).  
- Close unnecessary ports.  
- Regularly patch systems.  

---

# 3. SQL Injection (SQLi)  
**Definition**: Exploiting vulnerabilities in web applications to manipulate SQL queries and access unauthorized data.  

### **How It Works**  
- Inject malicious SQL code into input fields (e.g., `' OR 1=1 -- `).  
- Bypass authentication or dump databases.  

### **Types of SQLi**  
1. **Classic SQLi**: Direct injection via user inputs.  
2. **Blind SQLi**: No direct error messages; infer results from behavior.  
3. **Error-Based SQLi**: Exploit database error messages.  

### **Techniques**  
- **Union-Based**: Use `UNION` to combine queries.  
  - Example: `' UNION SELECT username, password FROM users -- `  
- **Boolean-Based**: Use true/false conditions to extract data.  
- **Time-Based**: Delay responses to confirm vulnerabilities (e.g., `SLEEP(5)`).  

### **Tools**  
- **SQLMap**: Automated tool for detecting and exploiting SQLi.  
- **Burp Suite**: Intercept and modify HTTP requests.  
- **Havij**: User-friendly SQLi tool for beginners.  

### **Prevention**  
- Use **parameterized queries** or prepared statements.  
- Sanitize inputs (e.g., escape special characters).  
- Deploy **Web Application Firewalls (WAF)**.  

---

# Real-World Examples  
1. **Heartland Payment Systems (2008)**: SQLi led to 130M credit card breaches.  
2. **TalkTalk (2015)**: SQLi exploited to steal data of 157k customers.  

---

# Summary  
- **Footprinting**: Gather intel to plan attacks.  
- **Network Scanning**: Map live hosts, ports, and vulnerabilities.  
- **SQLi**: Exploit poor input validation to manipulate databases.  

**Best Practices**: Regular audits, input validation, and employee training.  

---  

