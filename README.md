Task 4: Setup and Use a Firewall on Windows
Objective
Configure and test basic firewall rules to allow or block specific network traffic, demonstrating practical firewall management on a Windows system.

Tools Used
Windows Defender Firewall with Advanced Security (inbuilt tool in Windows)

Telnet Client (optional feature for testing blocked ports)

Steps Performed
1. Opened Firewall Configuration Tool
Pressed Windows + R → typed wf.msc → Enter.

2. Listed Current Firewall Rules
Viewed Inbound Rules and Outbound Rules in the Windows Defender Firewall console.

3. Created a Rule to Block Port 23 (Telnet)
Inbound Rules → New Rule

Port → TCP → Specific local ports: 23

Block the connection

Applied to Domain, Private, Public

Named rule Block Telnet

4. Enabled Telnet Client for Testing
Installed via Control Panel → Turn Windows features on or off → Check “Telnet Client”.

5. Tested the Rule
cmd
Copy code
telnet localhost 23
Result: Connection failed — confirming the firewall block worked.

6. Allowed SSH (Optional)
Created inbound rule for TCP port 22 with Allow the connection.

7. Removed the Test Rule
Deleted Block Telnet from Inbound Rules to restore original state.

Commands Used
cmd
Copy code
wf.msc
dism /online /Enable-Feature /FeatureName:TelnetClient
telnet localhost 23
Screenshots
(Place your screenshots here — showing the Block Telnet rule in Inbound Rules and the failed Telnet connection in CMD)

Summary
Firewalls filter traffic by applying rules that match direction, protocol, port number, and IP address.

Inbound rules control what comes into the system.

Outbound rules control what leaves the system.

Blocking unused or insecure ports like Telnet (23) reduces attack surfaces and improves security.
