#### Navigation

[Back to Home 🏠](../README.md) | [Previous: Create an OU and Attach a GPO](step5.md) | [Next: **Step 7** Check Event Viewer for Logins](step7.md)

---

## Step 6 

### Edit the GPO and apply the following rules:

- 6.1: A message should appear whenever the computer starts (do not install unauthorized programs).
- 6.2: Prevent the user's access to CMD.
- 6.3: Add script to the user's login to map the share you created.
- 6.4: Disable the run command from the start menu.

### 6.1 Configure Logon Message via GPO

- Right-click on the newly created GPO in the Group Policy Management Console (GPMC).
- Select ‘Edit’.
- Expand the tree to Computer Configuration > Policies > Windows Settings > Security Settings > Local Policies > Security Options.
- Scroll to find ‘Interactive logon: Message text for users attempting to log on’.
- Double-click it to open its properties.
- Check the box to ‘Define this policy setting’.
- In the text box, type “Do not install unauthorized programs”.
- Click Apply and then OK.
- Open Command Prompt as Administrator.
- Type gpupdate /force and press Enter to force the policy update immediately.
- Restart Desktop2 to ensure the new settings take effect.
- This can be done manually or through a command if remote management tools are available.

---

![alt text](https://github.com/hcoco1/Career-Simulation-2/blob/main/images/step_6_1.png?raw=true)

---

---

![alt text](https://github.com/hcoco1/Career-Simulation-2/blob/main/images/step_6_2.png?raw=true)

---

---

![alt text](https://github.com/hcoco1/Career-Simulation-2/blob/main/images/step_6_3.png?raw=true)

---

### 6.2 Disable Command Prompt via GPO


- Right-click on your Group Policy Object in the Group Policy Management Console (GPMC).
- Select ‘Edit’.
- Navigate to System Policies
- In the Group Policy Management Editor, navigate to User Configuration > Policies > Administrative Templates > System.
- Find and double-click on ‘Prevent access to the command prompt’.
- Enable the Policy
- In the settings window that opens, click on Enabled.
- Click Apply and then OK to save the changes.
- Update Group Policy and Restart
- Open Command Prompt as Administrator.
- Execute the command gpupdate /force to update the group policy settings immediately.
- Restart Desktop2 to ensure that the new settings take effect.

---

![alt text](https://github.com/hcoco1/Career-Simulation-2/blob/main/images/step_6_2_1.png?raw=true)

---
---

![alt text](https://github.com/hcoco1/Career-Simulation-2/blob/main/images/step_6_2_2.png?raw=true)

---

### 6.3: Add script to the user's login to map the share you created

- Right-click the shared folder at `\\EC2AMAZ-L3OOUG8\Sales` and click "Properties" to obtain the network path.
- Open a script editor like Notepad.
- Create a batch file (.bat) with the `net use Z: \\EC2AMAZ-L3OOUG8\Sales` command. Replace `Z:` with the desired drive letter and update the domain, username, and password with the appropriate credentials.
- Save the file as `map.bat`.
- Execute `map.bat` on the server to ensure it correctly maps the network drive.
- Open the Group Policy Management Console (GPMC).
- Expand the "Group Policy Objects" in the appropriate domain and navigate to the Sales OU.
- Right-click the Sales OU and select "Create a GPO and link it here." Name something relevant to the GPO, like "Map Network Drive for Sales."
- Edit the newly created GPO.
- Navigate to `User Configuration > Windows Settings > Scripts (Logon/Logoff) > Logon`.
- Double-click on Logon to open the properties. Click "Add" and then "Browse" to select the `map.bat` file previously created.
- After adding the script, click "OK" to close all dialogs.
  On a client computer in the Sales OU, run `gpupdate` at the command prompt to force the policy update and verify that the script runs at user logon.
- Log in to a test user account that is part of the Sales OU.
- Before login, verify there is no mapped network drive.
- After login, check that the `Z:` drive appears and contains the sales data, indicating that the mapping was successful.

---

![alt text](https://github.com/hcoco1/Career-Simulation-2/blob/main/images/step_6_3_1.png?raw=true)

---

### 6.4: Remove Run Command from Start Menu via GPO


- Right-click on your Group Policy Object in the Group Policy Management Console (GPMC).
- Select ‘Edit’.
- Navigate to Start Menu Policies
- In the Group Policy Management Editor, navigate to User Configuration > Policies > Administrative Templates > Start Menu and Taskbar.
- Scroll to find and double-click on ‘Remove Run menu from Start Menu’.
- In the properties window that opens, click on Enabled.
- Click Apply and then OK to save the changes.
- Open Command Prompt as Administrator.
- Type gpupdate /force and press Enter to force the policy update immediately.
- Restart ADMINISTRATOR to ensure that the new settings take effect.

---

![alt text](https://github.com/hcoco1/Career-Simulation-2/blob/main/images/step_6_4_1.png?raw=true)

---
---

![alt text](https://github.com/hcoco1/Career-Simulation-2/blob/main/images/step_6_4_2.png?raw=true)

---

#### Navigation

[Back to Home 🏠](../README.md) | [Previous: Create an OU and Attach a GPO](step5.md) | [Next: **Step 7** Check Event Viewer for Logins](step7.md)

