# WARNING

This is basically obsolete and there is a far better and less hacky solution available here:
https://github.com/jamesstringerparsec/Easy-GPU-PV
# Windows-Sandbox-Gaming-Guide
This is a guide to making a mostly persistent Windows Sandbox and also using it for gaming :)

Keep in mind that this still uses RDP which is limited to outputting at around 30 fps. Though it seems running games at higher frame rates makes it smoother and displays with BFI (Black Frame Insertion) improves the experience.

# Things to know

The folders that persist after closing and reopening "Sandboxed Gaming.wsb" are the following:

* C:\Program Files
* C:\Program Files (x86)
* C:\ProgramData
* C:\Users\WDAGUtilityAccount\AppData
* C:\Users\WDAGUtilityAccount\Desktop
* C:\Users\WDAGUtilityAccount\Documents
* C:\Users\WDAGUtilityAccount\Downloads
* C:\Users\WDAGUtilityAccount\Links
* C:\Users\WDAGUtilityAccount\Music
* C:\Users\WDAGUtilityAccount\Pictures
* C:\Users\WDAGUtilityAccount\Videos

Any other folder not listed there is NOT saved when you close it

# Prerequisites

From Microsoft https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-sandbox/windows-sandbox-overview#prerequisites

* Windows 10 Pro, Enterprise or Education build 18305 or Windows 11 (Windows Sandbox is currently not supported on Windows Home edition)
* AMD64 or (as of Windows 11 Build 22483) ARM64 architecture
* Virtualization capabilities enabled in BIOS
* At least 4 GB of RAM (8 GB recommended)
* At least 1 GB of free disk space (SSD recommended)
* At least two CPU cores (four cores with hyperthreading recommended)

Having Windows Sandbox enabled https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-sandbox/windows-sandbox-overview#installation

Download all three of these files:

* https://github.com/Soup333/Windows-Sandbox-Gaming-Guide/blob/main/run%20first.wsb
* https://github.com/Soup333/Windows-Sandbox-Gaming-Guide/blob/main/Sync.bat
* https://github.com/Soup333/Windows-Sandbox-Gaming-Guide/blob/main/Sandboxed%20Gaming.wsb

# Setup

After downloading "run first.wsb" and "Sandboxed Gaming.wsb", open those files in notepad (right click, open with notepad) to edit them.
You have to replace the parts that say "username" (no quotation marks) to your Windows User's username (this can be found by opening File Explorer and clicking on This PC, Local Disk (C:), Users, then finding your username's folder's name which you should recognize)

After replacing those, you will have to open This PC, Local Disk (C:), Users, then your username's folder and creating a new folder in it called "Sandboxed Gaming" without quotes. The "Sandboxed Gaming.wsb" Windows Sandbox and the programs running in it will have access to that folder and its contents and nothing else on your system and its used to store its files.

Now, run "run first.wsb" by double clicking on it. Windows Sandbox should open using the configuration of "run first.wsb".
You should see File Explorer open in Windows Sandbox, click on the top middle "View" button, then "Show", and click on "Hidden items". That lets you see the ProgramData folder. 

Now, in the same Windows Sandbox copy "Program Files", "Program Files (x86)", "ProgramData", and "Users" folders to the folder at the top named "COPY ProgramData, Program Files, Program Files (x86), Users, HERE".

If while copying them it says you can't copy a certain folder just press skip, and if it says wether to replace files or not then also press skip.

After ALL the folders are succesfully copied to the top "COPY ProgramData, Program Files, Program Files (x86), Users, HERE" folder close Windows Sandbox.

Now, on your PC (not Windows Sandbox) copy the Sync.bat you downloaded and open This PC, Local Disk (C:), Users, then your username's folder, Sandboxed Gaming, Users, WDAGUtilityAccount, Desktop, and finally paste the Sync.bat inside the Desktop folder.

Now, you can move "Sandboxed Gaming.wsb" to your PC's Desktop for quick access to it.

# Usage

Boom done you just set it up, nice :), now you can just double click on "Sandboxed Gaming.wsb" to open the sandboxed gaming Windows Sandbox and you should be able to get games supporting directx running. I for one installed steam on it and I only really tested 1 game but others should work since it uses Microsoft's WARP for running directx games
* https://docs.microsoft.com/en-us/windows/win32/direct3darticles/directx-warp#what-is-warp 

# Tips

* In my testing, 60 fps and potentially higher is smoother than leaving games at 30 fps / vsync
* You should definetly increase the amount of RAM it gets by modifying "Sandboxed Gaming.wsb" MemoryInMB> value </MemoryInMB to something like 8000 or more MB if you have enough RAM. It greatly improves performance.
* Also lower resolutions may also be smoother, not sure about this one
* If your monitor has a BFI option, maybe called PureXP, ULMB, ELMB, Blur reduction, etc, then try turning it on. It may improve the clarity.

# If there are any issues or if you have a way of improving it, open a new issue :o
