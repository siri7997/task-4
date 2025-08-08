 🔐 Task 4: Setup and Use a Firewall on Windows
🎯 Objective
Configure and test basic firewall rules to allow or block specific network traffic, demonstrating practical firewall management on a Windows system.

🧰 Tools Used
🛡️ Windows Defender Firewall with Advanced Security (inbuilt tool in Windows)

🖥️ Telnet Client (optional feature for testing blocked ports)

🛠️ Steps Performed
🔓 Opened Firewall Configuration Tool
⤷ Press Windows + R → type wf.msc → hit Enter

📄 Listed Current Firewall Rules
⤷ Viewed Inbound Rules and Outbound Rules in the Windows Defender Firewall console.

🚫 Created a Rule to Block Port 23 (Telnet)
⤷ Navigation: Inbound Rules → New Rule

Type: Port

Protocol: TCP

Specific local ports: 23

Action: Block the connection

Profile: Domain, Private, Public

Rule name: Block Telnet

✅ Enabled Telnet Client for Testing
⤷ Control Panel → Turn Windows features on or off → ☑️ Check Telnet Client

🧪 Tested the Rule

telnet localhost 23
Result: ⚠️ Connection failed — confirms firewall block is effective.

🔓 Allowed SSH (Optional)
⤷ Created inbound rule for TCP port 22 → Allow the connection

🧹 Removed the Test Rule
⤷ Deleted Block Telnet from Inbound Rules to restore original state.

💻 Commands Used
wf.msc
dism /online /Enable-Feature /FeatureName:TelnetClient
telnet localhost 23
📸 Screenshots
(Place your screenshots here — showing the "Block Telnet" rule in Inbound Rules and the failed Telnet connection in CMD)

🧠 Summary
🔐 Firewalls filter traffic by applying rules based on:

➡️ Direction (Inbound/Outbound)

🌐 Protocol (TCP/UDP)

🔢 Port Number

🧭 IP Address

✅ Inbound Rules control what enters the system

🔁 Outbound Rules control what exits the system

🔒 Blocking unused or insecure ports (like Telnet – port 23):

➖ Reduces attack surface

🔼 Improves overall system security
