
# 🔐 Cybersecurity Internship – Task 4: Setup and Use a Firewall on Windows

## 🎯 Objective
Configure and test basic firewall rules to allow or block traffic.

## 🧰 Tools Used
- Windows Defender Firewall
- Command Prompt (CMD)
- GitHub (for documentation upload)

## 🛠 Steps Performed

1. Opened **Windows Defender Firewall**.
2. Navigated to **Advanced Settings** → **Inbound Rules**.
3. Created a **New Rule**:
   - Rule Type: Port
   - Protocol: TCP
   - Port: 23 (Telnet)
   - Action: Block the connection

4. Tested the rule using Command Prompt:
   - Ran: `telnet 127.0.0.1 23`
   - Initially received: `Error: 740 - Elevated permissions are required`
   - Enabled Telnet using:
     ```
     dism /online /Enable-Feature /FeatureName:TelnetClient
     ```
   - Re-ran telnet and received:
     `Connecting To 127.0.0.1...Could not open connection to the host, on port 23: Connect failed`

   ✅ This confirms the firewall rule was successfully blocking the Telnet port.

## ✅ Conclusion
Using Windows Defender Firewall, we were able to block a service port (Telnet - Port 23) and confirm it with a live connection test. This demonstrates a basic yet critical approach to securing network services and minimizing attack surface.

---
> 📄 Screenshots and testing steps are included in the attached Word document: `Cybersecurity Internship - Task 4.docx`.
