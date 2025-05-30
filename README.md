# -Firewall-on-Windows-Linux
1.Linux (Kali) – Using UFW
Enabled UFW:
sudo ufw enable

Checked Status
sudo ufw status numbered

Blocked Telnet Port 23
sudo ufw deny 23

Tested Telnet
telnet localhost 23

Output: Connection refused (means the block worked)

Allowed SSH Port 22
sudo ufw allow 22

Removed Block Rule for Port 23
sudo ufw delete deny 23


2.Windows Firewall – Using GUI
-Opened Windows Defender Firewall with Advanced Security
-Start → Run → wf.msc
-Clicked Inbound Rules → New Rule
-Selected Port → TCP → Entered 23
-Chose "Block the connection"
-Applied to Domain, Private, Public → Named it "Block Telnet"
-Confirmed "Block Telnet" rule was added
-Screenshot taken and saved

Deleted "Block Telnet" rule
Right-click → Delete
Final screenshot taken to confirm rule is gone
