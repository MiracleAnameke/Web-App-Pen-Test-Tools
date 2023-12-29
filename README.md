# Web Security
## Web App Pen Test Tools

### Lab Requirements
- Internet connectivity & VMware Workstation version 15.5.7 or above.

### Virtual Machines used:
- Kali Linux VM
- Ubuntu Web Server VM
- Windows 10 VM
- Windows Server 2016 VM
- Metasploit (MSF VM)

### Lab Overview
This Lab is focused on the utilization of various web application penetration testing tools. It covers tasks from modifying HTTP headers to website mirroring and command injection challenges, providing a comprehensive practice for identifying and exploiting web application vulnerabilities.

### Lab Tasks and Screenshots

### Part 01: Change the User-Agent HTTP Header in Firefox
**Task**: Modify the User-Agent Header in the HTTP packet to include custom information.
- **Steps**:
    1. Load Mutillidae on Kali Linux's Firefox and capture packets using Burp Suite.
    2. Modify the User-Agent header to reflect your FOLusername as the page loads.
- **Slide 01**: Screenshot showing the modified User-Agent Header and its effect on the Mutillidae application.
    <img src="https://i.imgur.com/3Ufs0fH.png" height="400px" width="auto" alt="User-Agent HTTP Header Change"/>

### Part 02: Use User-Agent Switcher and Manager

**Objective**: Use a browser add-on to change the User-Agent header and capture the modified HTTP request using Burp Suite.

**Steps**:
1. **Add-on Installation**: Install a User-Agent Switcher and Manager add-on in Firefox.
2. **Mutillidae User Setup**: Create a new user with your `FOLusername` in Mutillidae and login.
3. **Modify User-Agent**: Customize the User-Agent field to inject JavaScript displaying date, time, and cookie information.
4. **Capture Request**: Use Burp Suite to capture the HTTP request with the modified User-Agent header.

**Expected Outcome**:
- The User-Agent header is customized and captured reflecting JavaScript payload.
- Mutillidae reflects any changes if susceptible to header injection.

**Slide 02**: Screenshot of Burp Suite showing the modified User-Agent in the HTTP request and any visible impact on Mutillidae.

<img src="https://i.imgur.com/znqNbTZ.png" height="400px" width="auto" alt="User-Agent Modification and Capture"/>


### Part 02: Skipfish
**Task**: Utilize skipfish to perform automated web application security reconnaissance.
- **Steps**:
    1. Run skipfish with a custom command targeting Juice Shop URL for a comprehensive scan.
- **Slide 03**: Screenshot showing the results of the skipfish scan.
    <img src="https://i.imgur.com/OjEvJpc.png" height="400px" width="auto" alt="Skipfish Results"/>

### Part 03: Golismero
**Task**: Conduct a vulnerability scan using Golismero.
- **Steps**:
    1. Run Golismero against the Mutillidae web application to find potential vulnerabilities.
- **Slide 04**: Screenshot showing the output of the Golismero scan and the command used.
    <img src="https://i.imgur.com/iyYHGXI.png" height="400px" width="auto" alt="Golismero Output"/>

### Part 04: Nikto
**Task**: Use Nikto to scan and identify vulnerabilities in a DVWA hosted on a server.
- **Steps**:
    1. Run Nikto against the host and capture the results.
- **Slide 05**: Screenshot showing the Nikto output and the command constructed.
    <img src="https://i.imgur.com/P56IGqO.png" height="400px" width="auto" alt="Nikto Scan Results"/>

### Part 05: Mirror websites with HTTrack
**Task**: Create a mirror of web applications using HTTrack for offline analysis.
- **Steps**:
    1. Use HTTrack to mirror specific sites and inspect the files that were copied.
- **Slide 06**: Screenshot showing the files mirrored by HTTrack.
    <img src="https://i.imgur.com/Xf7QOR0.png" height="400px" width="auto" alt="HTTrack Mirroring"/>

### Part 06: Challenge: Command injection in DVWA
**Task**: Execute a command injection attack on the DVWA and adjust inputs to bypass security controls.
- **Steps**:
    1. Exploit the Command Execution page on DVWA to inject and execute commands.
    2. Adjust the input to bypass additional security controls and return the output of the hostname command.
- **Slide 07**: Screenshot showing the input command, output from the server, the security level, and the URL.
    <img src="https://i.imgur.com/uB239Bg.png" height="400px" width="auto" alt="Command Injection Challenge"/>


**Conclusion**: This lab offers a hands-on approach to using various web application penetration testing tools, highlighting the importance of regular security checks and vulnerability assessments in maintaining robust web application security.
