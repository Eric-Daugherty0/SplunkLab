# SplunkLab
Hunting malware in my Splunk home lab
I’ve been practicing blue team skills, and this week I ran a threat hunt in my Splunk lab using Sysmon logs.
Here’s what I did:
Checked network connections (Event ID 3) to see which machines were talking to outside IPs.
Checked file creation (Event ID 11) and noticed executables and scripts being dropped in an odd folder, C:\Games, plus an .exe in a user’s Temp folder.
Pulled the file hash from the suspicious event.
Looked it up in VirusTotal. 24 of 47 vendors flagged it as malicious, a remote access trojan disguised as an invoice file.
What I learned:
Sysmon and Splunk give great visibility into what’s happening on a machine.
Odd file locations are a good place to start hunting.
Checking a hash in threat intel can quickly confirm a suspicion.
I’m continuing to build my SOC analyst skills
