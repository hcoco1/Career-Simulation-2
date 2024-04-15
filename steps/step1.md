##### Navigation

[Back to Home 🏠](../README.md) | [Next: Create a User for the New Hire](step2.md)

---

## Step 1

### Join the Computer to the Domain contoso.com

- On the server VM, run on PowerShell `ipconfig` and copy the IP from the IPv4 Address.

```powershell
C:\Users\fstack>ipconfig

Windows IP Configuration


Ethernet adapter Ethernet 2:

   Connection-specific DNS Suffix  . : us-west-2.compute.internal
   Link-local IPv6 Address . . . . . : fe80::1842:e2ee:d867:e4a5%2
   IPv4 Address. . . . . . . . . . . : 172.31.6.168
   Subnet Mask . . . . . . . . . . . : 255.255.240.0
   Default Gateway . . . . . . . . . : 172.31.0.1

Tunnel adapter Local Area Connection* 3:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Tunnel adapter isatap.us-west-2.compute.internal:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . : us-west-2.compute.internal
```

---

![Step 1](https://github.com/hcoco1/career-2/blob/main/images/step_1.png?raw=true)

---

- On the desktop-2 VM, click the search icon and type "network connection"

- Click on "View network connections".
- Right-click the current network connection and select "Properties".
- Double-click on "Internet Protocol Version 4 (TCP/IPv4)".
- Select "Use the following DNS server addresses".
- Enter the IP address of the domain controller in the "Preferred DNS server" box.
- Click "OK" twice to exit out of the adapter settings.

---

![Step 1](https://github.com/hcoco1/career-2/blob/main/images/step_1_2.png?raw=true)

---

- Right-click the Start menu on the new user's desktop PC and select "System".
- Click on "Rename this PC (advanced)" on the far right of the window.
- Click on "Change".
- Enter the username you created under "Computer name".
- Select "Domain" under "Member of" and type "contoso.com".
- Enter the domain's credentials `administrator/Pa$$w0rd` and click "OK"
- Restart the computer so the changes take effect.

---

![Step 1](https://github.com/hcoco1/career-2/blob/main/images/step_1_7.png?raw=true)

---

##### Navigation

[Back to Home 🏠](../README.md) | [Next: Create a User for the New Hire](step2.md)
