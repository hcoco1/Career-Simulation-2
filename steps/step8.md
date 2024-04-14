## Step 8
### Use PowerShell to check what the latest program installed on the computer was

- Open the PowerShell 
- Type the following command


```PowerShell
Get-WmiObject -Class Win32_Product | Sort-Object InstallDate -Descending | Select-Object -First 1 Name, InstallDate
```

---

![alt text](https://github.com/hcoco1/career-2/blob/main/images/step_8_1.png?raw=true)

---

## Navigation

[Previous: Check Event Viewer for Logins](step7.md) | [Next: List All Running Services](step9.md)

