# Windows-Sandbox-Gaming-Guide
This is a guide to making a persistent Windows Sandbox and also using it for gaming

Keep in mind that this still uses RDP which is outputting at around 30 fps. Though it seems running games at higher frame rates make it smoother and displays with BFI (Black Frame Insertion) improves the experience.

# Prerequisites

From Microsoft https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-sandbox/windows-sandbox-overview#prerequisites

* Windows 10 Pro, Enterprise or Education build 18305 or Windows 11 (Windows Sandbox is currently not supported on Windows Home edition)
* AMD64 or (as of Windows 11 Build 22483) ARM64 architecture
* Virtualization capabilities enabled in BIOS
* At least 4 GB of RAM (8 GB recommended)
* At least 1 GB of free disk space (SSD recommended)
* At least two CPU cores (four cores with hyperthreading recommended)

Having Windows Sandbox enabled https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-sandbox/windows-sandbox-overview#installation

Download both these .wsb Windows Sandbox config files

* https://github.com/Soup333/Windows-Sandbox-Gaming-Guide/blob/main/run%20first.wsb
* https://github.com/Soup333/Windows-Sandbox-Gaming-Guide/blob/main/Sandboxed%20Gaming.wsb

# Setup

After downloading run first.wsb and Sandboxed Gaming.wsb, open those files in notepad (right click, open with notepad) to edit them.
You have to replace the parts that say "username" (no quotation marks) to your Windows User's username (this can be found by opening File Explorer and clicking on Local Disk (C:), Users, then finding your username's folder which you should recognize)

After replacing those, you will have to open Local Disk (C:), Users, then your username's folder and creating a new folder in it called "Sandboxed Gaming" without quotes. The "Sandboxed Gaming.wsb" Windows Sandbox will have access to that folder and its contents but nothing else on your system.

Now, click on 
