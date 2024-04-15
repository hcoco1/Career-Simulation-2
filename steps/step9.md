##### Navigation

[Back to Home 🏠](../README.md) | [Previous: Check the Latest Installed Program](step8.md) | [Next: Summary](summary.md)

---

## Step 9

### Write a PowerShell script that gives a list of all running services and puts it in a file named running_services.txt.

- Search for Notepad in the Start menu and open it.
- Type the PowerShell Command

```PowerShell
Get-WmiObject -Class Win32_Product | Select-Object -Property Name, Version, InstallDate > C:\Users\fstack\Desktop\running_services.txt
```

- Click File > Save As.
- In the Save As dialog, change the Save as type to All Files.
- Name the file with a .ps1 extension, for example, list_installed_programs.ps1.
- Save the file to a convenient location where you can easily access it.
- Run the PowerShell Script
- Open File Explorer and navigate to the location where you saved your .ps1 script file.
- Right-click on the PowerShell script file.
- Select ‘Run with PowerShell’.
- If prompted by User Account Control (UAC), click Yes to allow the script to run.
- Navigate to C:\Users\fstack\Desktop on your computer.
- Look for the running_services.txt file. This file should contain the list of all installed products along with their version and installation date.

---

![alt text](https://github.com/hcoco1/Career-Simulation-2/blob/main/images/step_9_1.png?raw=true)

---
---

![alt text](https://github.com/hcoco1/Career-Simulation-2/blob/main/images/step_9_2.png?raw=true)

---
---

![alt text](https://github.com/hcoco1/Career-Simulation-2/blob/main/images/step_9_3.png?raw=true)

---
---

![alt text](https://github.com/hcoco1/Career-Simulation-2/blob/main/images/step_9_4.png?raw=true)

---

##### Navigation

[Back to Home 🏠](../README.md) | [Previous: Check the Latest Installed Program](step8.md) | [Next: Summary](summary.md)

