#### Navigation

[Back to Home 🏠](../README.md) | [Previous: Create and Share Department Folder](step4.md) | [Next: **Step 6** Edit GPO and Apply Rules](step6.md)

---


## Step 5

### Create an OU with the department's name and place the user, group, and computer in the OU. Attach a GPO to the OU you created.

### Access Group Policy Management Console

- Click on the search bar at the bottom left of your screen.
- Type gpmc.msc and press Enter. This opens the Group Policy Management Console.

---

![alt text](https://github.com/hcoco1/Career-Simulation-2/blob/main/images/step_5_1.png?raw=true)

---

### Create New Organizational Unit

- In the left panel of the GPMC, right-click on your domain (e.g., contoso.com).
- Select New Organizational Unit.
- Enter a name for your OU and click OK.

### Organize Resources within OU


- Locate the user and group you created earlier (from Step 3).
- Drag and drop both the user and the group into the newly created OU folder.

- Find ADMINISTRATOR in the Active Directory list.
- Drag and drop ADMINISTRATOR into the same OU folder.

### Create and Link a GPO

- Right-click on the OU folder you created.
- Select Create a GPO in this domain, and Link it here.
- Provide a name for the new GPO.
- Click OK to create and link the GPO to your OU.
---

![alt text](https://github.com/hcoco1/Career-Simulation-2/blob/main/images/step_5_2.png?raw=true)

---

#### Navigation

[Back to Home 🏠](../README.md) | [Previous: Create and Share Department Folder](step4.md) | [Next: **Step 6** Edit GPO and Apply Rules](step6.md)

