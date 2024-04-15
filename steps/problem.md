##### Navigation

[Back to Home 🏠](../README.md) | [Introduction](introduction.md)

---



## Scenario
As a new StackFull Software employee, you've been tasked to work alongside Damen, the IT Security Manager, to write a runbook for the IT Pre-onboarding process.

IT onboarding introduces and trains new hires in the technology they'll use in their day-to-day responsibilities. Before onboarding begins, however, the IT team needs to set up and ensure new hire technology is ready for their first day.
A runbook is a detailed "how-to" guide for completing a commonly repeated task or procedure within a company's IT operations process, like setting up a laptop for a new hire.
You have the unique experience of participating in IT onboarding and knowledge of Windows management that can help with this task! Complete each of the steps below using the server and DESKTOP-2 in your Unit 5: Windows VM, then write a runbook to complete the steps for all new hires moving forward.

## Problem
Before you begin, decide with your group:

Name of the new hire
Non-technical role at StackFull Software (i.e., recruiter, sales associate, social media associate)
Department they work in (i.e., HR, Sales, Marketing)
Read the steps below and discuss how each step may differ based on the permissions needed for your specific new hire. 

Step 1
- Join the computer to the domain (the domain name is contoso.com). The username/password is administrator/Pa$$w0rd.

Step 2
- Switch to the server. Create a user for the new hire and set a password.

Step 3
- Create a group with the department name and place the user in that group.

Step 4
- Create a share on the server with the department name and share it only with people who belong to that department (read and write permissions). In the folder, create a text document called test.txt.

Step 5
- Create an OU with the department's name and place the user, group, and computer in the OU. Attach a GPO to the OU you created.

Step 6
- Edit the GPO and apply the following rules:

A message should appear whenever the computer starts (do not install unauthorized programs).
- Prevent the user's access to CMD.
- Add script to the user's login to map the share you created.
- Disable the run command from the start menu.
Step 7
- Check the Event Viewer on the server machine and write down the last successful login from your user. (Note: You must log in with the domain administrator account).

Step 8
- Use PowerShell to check what the latest program installed on the computer was.

Step 9
- Write a PowerShell script that gives a list of all running services and puts it in a file named running_services.txt.

Runbook
Damen would like you to write a runbook documenting your process for setting up a machine for new hires. Your runbook should include the following:

- Introduction of what steps the runbook achieves
- Procedure on how to complete steps, with visuals
  
--- 

##### Navigation

[Back to Home 🏠](../README.md) | [Introduction](introduction.md)