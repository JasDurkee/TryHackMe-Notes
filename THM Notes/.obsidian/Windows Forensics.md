**<h3>Registry Editor</h3>**
	+ <strong>OS-Version</strong>: SOFTWARE\Microsoft\Windows NT\CurrentVersion
	---
	+ <strong>Computer Name</strong>: SYSTEM\CurrentControlSet\Control\ComputerName\ComputerName
	---
	+ <strong>Time Zone Information</strong>: SYSTEM\CurrentControlSet\Control\TimeZoneInformation
	---
	+ <strong>Network Interfaces and Past Networks</strong>: SYSTEM\CurrentControlSet\Services\Tcpip\Parameters\Interfaces
	---
	+<strong>Autostart Programs (Autoruns):</strong> SYSTEM\CurrentControlSet\Services
	If the `start` key is set to 0x02, this means that this service will start at boot
	---
	+<strong>SAM hive and user information:</strong> The SAM hive contains user account information, login information, and group information. This information is mainly located in the following location: SAM\Domains\Account\Users
	---
	+<strong>Recent Files opened for each user:</strong> NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Explorer\RecentDocs
	To look for specific file extensions, add .\<fileExtension> after \RecentDocs\.\<fileExtension>
	+<strong>UserAssist: Keeps track of applications launched by the user</strong> NTUSER.DAT\Software\Microsoft\Windows\Currentversion\Explorer\UserAssist\{GUID}\Count


**<h3>External Devices</h3>**
	+<strong>Device Identification:</strong> These locations keep track of USB keys plugged into a system:
		- SYSTEM\CurrentControlSet\Enum\USBSTOR
		- SYSTEM\CurrentControlSet\Enum\USB
	+<strong></strong>
	
