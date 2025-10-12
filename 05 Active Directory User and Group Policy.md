
<!-- Your monitor number = #$34T# -->

# 💡 Modify Active Directory Users and Computers

### 1. On Server Manager
Go to Manage > `Active Directory Users and Computers` __[01]__

<br>

![01-AD Users](<img/00 AD-Users-01.png>)

&nbsp;
---
&nbsp;

### 2. Modify Active Directory
Drop down the existing domain controller, in this example is `rivan92.com` __[02]__  
Then, on the `Users` __[03]__ directory, add a `New Object - User` __[04]__

<br>

![02-AD Users](<img/00 AD-Users-02.png>)

&nbsp;
---
&nbsp;

### 3. New Object - User
Assign the following user details __[05]__
- First name: `Anne`
- Last name: `Curtis`
- Initials: `C`
- Full name: `Anne C. Curtis`

<br>

Then, the user login name: `ac` __[06]__

<br>

Then, select `Next` __[07]__

<br>

![03-AD Users](<img/00 AD-Users-03.png>)

&nbsp;
---
&nbsp;

### 4. Set User Password
Assign a password. In this example it is `C1sc0123` __[08]__  
- Uncheck `User must change password at next logon` __[09]__
- Select `Password never expires` __[10]__

<br>

Then, select `Next` __[11]__

<br>

![04-AD Users](<img/00 AD-04.png>)

&nbsp;
---
&nbsp;

### 5. Confirm New User
Select `Finish` __[12]__
<br>

![05-AD Users](<img/00 AD-Users-05.png>)

&nbsp;
---
&nbsp;

### 6. Create an OU (Organizational Unit)
Select, then right-click on the domain controller, in this case it's `rivan92.com` __[13]__,
then `New` __[14]__ > `Organizational Unit` __[15]__

<br>

![06-AD Users](<img/00 AD-Users-06.png>)

&nbsp;
---
&nbsp;

### 7. New Object - Organizational Unit
Set `NOC` __[16]__ as the name of the OU. Then, select `OK` __[17]__

<br>

![07-AD Users](<img/00 AD-Users-07.png>)

&nbsp;
---
&nbsp;

### 8. Create a Group
> [!IMPORTANT]
> Select the OU

Select `NOC` __[18]__. Then click on the `Create a new group icon` __[19]__

<br>

![08-AD Users](<img/00 AD-Users-08.png>)

&nbsp;
---
&nbsp;

### 9. New Object - Group
Add a Group Name: `Global-NOC` __[20]__  & __[21]__  
The, select `OK` __[22]__

<br>

![09-AD Users](<img/00 AD-Users-09.png>)

&nbsp;
---
&nbsp;

### 10. Create a new Local Group
Click on the `Create a new group icon` __[23]__ again
<br>

![10-AD Users](<img/00 AD-Users-10.png>)

&nbsp;
---
&nbsp;





### 11. Wait for the Feature to install successfully.
<br>

![11-AD](<img/00 AD-11.png>)

&nbsp;
---
&nbsp;

### 12. Promote the server
Once installation is finished, `Promote this server to a domain controller` __[11]__
<br>

![12-AD](<img/00 AD-12.png>)

&nbsp;
---
&nbsp;

### 13. Deployment Configuration
Select `Add a new forest` __[12]__  

<br>

The Root domain name must be based on the suffix that is set on the server's network adapter.  
To identify that prefix, press `Win + R` to access `Run` __[13]__  
- Type `ncpa.cpl` __[14]__.
- Then, `OK` __[15]__.

<br>

> [!NOTE]
> Refer to the setup for Windows Server 2022. These settings should have already been set prior to installing Active Directory.

<br>

![13-AD](<img/00 AD-13.png>)

&nbsp;
---
&nbsp;

### 14. Identify the Root Domain Name
`Right-click` on the network adapter that connects to the network, in this case its `TunayNaLAN` __[16]__. 

<br>

Next, select `Properties` __[17]__

<br>

![14-AD](<img/00 AD-14.png>)

&nbsp;
---
&nbsp;

### 15. Network Adapter Properties
Select `Internet Protocol Version 4 (TCP/IPv4)` __[18]__.  
Then, `Properties` __[19]__.

<br>

![15-AD](<img/00 AD-15.png>)

&nbsp;
---
&nbsp;

### 16. IPv4 Properties
Verify that the necessary `IP addressing` is set on the Network Adapter __[20]__.

<br>

> [!IMPORTANT]
> The addressing set on this example is connected to a switch within the subnet of __10.#$34T#.1.0 /24__  
> If you do not have a switch or any external hardware, simply choose a Network Adapter that is connected to either NAT, or VMNet2. This way, you can configure AD with RADIUS for the CSR1000v for AAA.  
> As long as the IP address set on the adapter is within the same subnet as the VMNet, there should be no problems.
 
<br>

Then, select `Advanced..` __[21]__

<br>

![16-AD](<img/00 AD-16.png>)

&nbsp;
---
&nbsp;

### 17. DNS Settings
Go to `DNS` __[22]__

<br>

![17-AD](<img/00 AD-17.png>)

&nbsp;
---
&nbsp;

### 18. DNS Suffix
The DNS suffix set on the network adapter, in this case is `rivan92.com` __[23]__, must be set as the `Root Domain Name` __[24]__

<br>

![18-AD](<img/00 AD-18.png>)

&nbsp;
---
&nbsp;

### 19. Configure Deployment
Then, return to the installation window and select `Next` __[25]__

<br>

![19-AD](<img/00 AD-19.png>)

&nbsp;
---
&nbsp;

### 20. Domain Controller Options
`Enter a password` __[26]__ for the domain controller. This will be used to login to the account.

<br>

Then, select `Next` __[27]__

<br>

![20-AD](<img/00 AD-20.png>)

&nbsp;
---
&nbsp;

### 21. DNS Options
Select `Next` __[28]__

<br>

![21-AD](<img/00 AD-21.png>)

&nbsp;
---
&nbsp;

### 22. Additional Options
Simply wait for Windows to automatically set a `NetBIOS domain name` __[29]__

<br>

Then, select `Next` __[30]__

<br>

![22-AD](<img/00 AD-22.png>)

&nbsp;
---
&nbsp;

### 23. Paths
Select `Next` __[31]__

<br>

![23-AD](<img/00 AD-23.png>)

&nbsp;
---
&nbsp;


### 24. Review Options
Select `Next` __[32]__

<br>

![24-AD](<img/00 AD-24.png>)

&nbsp;
---
&nbsp;

### 25. Prerequisites Check
Select `Install` __[33]__

<br>

![25-AD](<img/00 AD-25.png>)

&nbsp;
---
&nbsp;

### 26. Log in to the Controller
After installation, Windows will restart, select `Close` __[34]__

<br>

![26-AD](<img/00 AD-26.png>)

&nbsp;
---
&nbsp;

### 27. Results
Wait for the installation to be finalized, then on next bootup, access the controller based on the password that was set. In this case, the password used is `C1sc0123` __[35]__

<br>

![27-AD](<img/00 AD-27.png>)

