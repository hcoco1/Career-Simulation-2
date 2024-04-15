#### Navigation

[Back to Home 🏠](../README.md) | [Previous: Edit GPO and Apply Rules](step6.md) | [Next: **Step 8** Check the Latest Installed Program](step8.md)

---

## Step 7

### Check the Event Viewer on the server machine and write down the last successful login from your user

- Open the Group Policy Management Console (GPMC).
- Right-click on the appropriate Organizational Unit (OU) or domain, then select “Create a GPO in this domain, and Link it here.”
- Name the new GPO appropriately related to event log handling.
- Navigate to: Computer Configuration > Policies > Windows Settings > Security Settings > Local Policies > Audit Policy.
- Double-click on Audit logon events.
- Check the “Define these policy settings” box.
- Enable “Success” to log successful events.
- Click Apply and OK.
- Open Command Prompt as an administrator.
- Type gpupdate /force and press Enter to update the group policy settings immediately.
- Go to the Control Panel > System and Security > Administrative Tools.
- Double-click on Event Viewer.
- In Event Viewer, on the left panel, navigate to Windows Logs > Security.
- Scroll through or filter the logs to find the last successful login event for your user.

---

![alt text](https://github.com/hcoco1/Career-Simulation-2/blob/main/images/step_7_1.png?raw=true)

---

---

![alt text](https://github.com/hcoco1/Career-Simulation-2/blob/main/images/step_7_0.png?raw=true)

---

#### Navigation

[Back to Home 🏠](../README.md) | [Previous: Edit GPO and Apply Rules](step6.md) | [Next: **Step 8** Check the Latest Installed Program](step8.md)

