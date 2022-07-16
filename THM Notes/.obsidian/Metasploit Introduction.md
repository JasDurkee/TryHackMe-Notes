**<h3>Metasploit Introduction</h3>**
+  Metasploit is a set of tools that allow information gathering, scanning, exploitation, exploit development, post-exploitation, and more
+  <strong>msfconsole:</strong> Main command line interface
+  <strong>Modules:</strong> Supporting modules such as exploits, scanners, payloads, etc.
+  <strong>Tools:</strong> Stand-alone tools that will help vulnerability research, vulnerability assessment, or penetration testing.

______
**<h3>Generic Terms</h3>**
______
- <strong>Exploit:</strong> A piece of code that uses a vulnerability present on the target system.
- <strong>Vulnerability:</strong> A design, coding, or logic flaw affecting the target system.
- <strong>Payload:</strong> An exploit will take advantage of a vulnerability, payloads are the code that will run on the target system.

______
**<h3>Features</h3>**
______

- <strong>Auxilary:</strong> Any supporting module, such as scanners, crawlers, and fuzzers, can be found here:![](https://tryhackme-images.s3.amazonaws.com/user-uploads/603df7900d7b6f1dff18b0bd/room-content/aaeb4ff4aa7fc33289b2bb581d874f16.png)
- <strong>Encoders:</strong> Encoders will allow you to encode the exploit and payload in the hope that a signature-based antivirus solution may miss them.![](https://tryhackme-images.s3.amazonaws.com/user-uploads/603df7900d7b6f1dff18b0bd/room-content/814490c07d05616009169c80cbb173a5.png)
- <strong>Evasion:</strong> While encoders will encode the payload, they should not be considered a direct attempt to evade antivirus software. ![](https://tryhackme-images.s3.amazonaws.com/user-uploads/603df7900d7b6f1dff18b0bd/room-content/fe66d8ad4c915fa496a20e6f6291a0ad.png)
- <strong>Exploits:</strong> Exploits, neatly organized by target system:![](https://tryhackme-images.s3.amazonaws.com/user-uploads/603df7900d7b6f1dff18b0bd/room-content/b940db3ff6ec430322206f2e161114fc.png)
- <strong>NOPs:</strong> Literally do nothing. ![](https://tryhackme-images.s3.amazonaws.com/user-uploads/603df7900d7b6f1dff18b0bd/room-content/71c6dee3ef13c5bc841aac92ce3253d7.png)
- <strong>Payloads:</strong> Code that will run on the target system. ![](https://tryhackme-images.s3.amazonaws.com/user-uploads/603df7900d7b6f1dff18b0bd/room-content/a4c9a90b50c7c46a6c8c1a5f78500ad1.png)
	- Three directories under payloads:
		- Singles: Self-contained payloads that do not need to download an additional component to run
		- Stagers: Responsible for setting up a connection channel between Metasploit and the target system
		- Stages: Downloaded by the stager. Allows you to use larger sized payloads
- <strong>Post:</strong> Useful on the final stage of the penetration testing process, post-exploitation. ![](https://tryhackme-images.s3.amazonaws.com/user-uploads/603df7900d7b6f1dff18b0bd/room-content/fa98b51a9b3862dc43eb0d3007057290.png)
___
**<h3>Msfconsole</h3>**
___
- Msfconsole will support most linux commands. 
- **DOES NOT SUPPORT OUTPUT REDIRECTION**
- <strong>Search command:</strong> This command will search the Metasploit framework database for modules relevant to the given search parameter. You can conduct searches using CVE numbers, exploit names (eternalblue, heartbleed, etc.), or target system.
	- <strong>Rank colomn:</strong> Exploits are rated based on their reliability. ![](https://tryhackme-images.s3.amazonaws.com/user-uploads/603df7900d7b6f1dff18b0bd/room-content/a88c8d37283878e01447853a68578deb.png)
- <strong><h4>Exploit Parameters:</h4></strong>
	- **RHOSTS:** “Remote host”, the IP address of the target system. A single IP address or a network range can be set. This will support the CIDR (Classless Inter-Domain Routing) notation (/24, /16, etc.) or a network range (10.10.10.x – 10.10.10.y). You can also use a file where targets are listed, one target per line using file:/path/of/the/target_file.txt
	- **RPORT:** “Remote port”, the port on the target system the vulnerable application is running on.
	- **PAYLOAD:** The payload you will use with the exploit.
	- **LHOST:** “Localhost”, the attacking machine (your AttackBox or Kali Linux) IP address.
	- **LPORT:** “Local port”, the port you will use for the reverse shell to connect back to. This is a port on your attacking machine, and you can set it to any port not used by any other application.
	- **SESSION:** Each connection established to the target system using Metasploit will have a session ID. You will use this with post-exploitation modules that will connect to the target system using an existing connection
- To set parameters, use the command "set `<parameter>` "
- <strong><h4>Portscanning Parameters:</h4></strong>
	- **CONCURRENCY:** Number of targets to be scanned simultaneously.
	- **PORTS:** Port range to be scanned. Please note that 1-1000 here will not be the same as using Nmap with the default configuration. Nmap will scan the 1000 most used ports, while Metasploit will scan port numbers from 1 to 10000.
	- **RHOSTS:** Target or target network to be scanned.
	- **THREADS:** Number of threads that will be used simultaneously. More threads will result in faster scans.
- <strong>UDP service identification:</strong> scanner/discovery/udp_sweep module will allow you to quickly identify services running over UDP.
- <strong>SMB Scans:</strong> scanner/smb/smb_version module allows you to identify smb
- <strong>Workspace:</strong> Allows you to have your own workspace and the ability to save your work into a database.
