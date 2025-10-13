
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

### 11. New Object - Group
Add a Group Name: `Local-NOC` __[24]__  & __[25]__  
Set the Group Scope as `Domain Local` __[26]__  
The, select `OK` __[27]__  

<br>

![11-AD Users](<img/00 AD-Users-11.png>)

&nbsp;
---
&nbsp;

### 12. Move User
Click on the `Users` __[28]__ directory. Then, drag the recently created user, `Anne C. Curtis` __[29]__, inside the OU, `NOC` __[30]__

<br>

![12-AD Users](<img/00 AD-Users-12.png>)

&nbsp;
---
&nbsp;

### 13. Don't show the warning
Select `Yes` __[31]__  

<br>

![13-AD Users](<img/00 AD-Users-13.png>)

&nbsp;
---
&nbsp;

### 14. User Membership
Select the OU, `NOC` __[32]__, then `Right-click` __[33]__ on Anne C. Curtis.   

<br>

Then select `Properties` __[34]__. 

![14-AD Users](<img/00 AD-Users-14.png>)

&nbsp;
---
&nbsp;

### 15. Modify Membership
On the `Member Of` __[35]__ tab, select `Add` __[36]__.

<br>

![15-AD Users](<img/00 AD-Users-15.png>)

&nbsp;
---
&nbsp;

### 16. Select Groups (Global)
Add the user to `Global-NOC` __[37]__ then select `OK` __[38]__.

![16-AD Users](<img/00 AD-Users-16.png>)

&nbsp;
---
&nbsp;

### 17. Primary Group
Select `Global-NOC` __[39]__. Then, `Set Primary Group` __[40]__

<br>

![17-AD Users](<img/00 AD-Users-17.png>)

&nbsp;
---
&nbsp;

### 18. Clear Membership
Select `Domain Users` __[41]__, then `Remove` __[42]__. Confirm the removal and select `Yes` __[43]__

<br>

![18-AD Users](<img/00 AD-Users-18.png>)

&nbsp;
---
&nbsp;

### 19. Confirm Member Of
Select `Apply` __[44]__

<br>

![19-AD Users](<img/00 AD-Users-19.png>)

&nbsp;
---
&nbsp;

### 20. Group Management
Select `Global-NOC` __[45]__ then `Properties` __[46]__

![20-AD Users](<img/00 AD-Users-20.png>)

&nbsp;
---
&nbsp;

### 21. Add Member Of
On the `Member Of` __[47]__ tab, `Add` __[48]__

<br>

![21-AD Users](<img/00 AD-Users-21.png>)

&nbsp;
---
&nbsp;

### 22. Select Groups (Local)
Add the user to `Local-NOC` __[49]__ then select `OK` __[50]__.

![22-AD Users](<img/00 AD-Users-22.png>)

&nbsp;
---
&nbsp;

### 23. Confirm Member Of
Select `OK` __[51]__

<br>

![23-AD Users](<img/00 AD-Users-23.png>)

<br>

![24-AD Users](<img/00 AD-Users-24.png>)

&nbsp;
---
&nbsp;

### 24. Modify Network Policy
Return to the Network Policy Server, then under `Policies` __[52]__, select `Network Policies` __[53]__ then right-click on the `Secure Wireless Connections` __[54]__ and select `Properties` __[55]__.

<br>

![25-AD Users](<img/00 AD-Users-25.png>)

&nbsp;
---
&nbsp;

### 25. Secure Wireless Connections Properties
On the `Conditions` __[56]__ tab. Select `Windows Groups` __[57]__, then `Edit` __[58]__.

<br>

![26-AD Users](<img/00 AD-Users-26.png>)

&nbsp;
---
&nbsp;

### 26. Windows Groups
`Add Groups...` __[59]__

<br>

![27-AD Users](<img/00 AD-Users-27.png>)

&nbsp;
---
&nbsp;

### 27. Select Group
Add `Local-NOC` __[60]__. Then, select `OK` __[61]__

<br>

![27-AD Users](<img/00 AD-Users-27.png>)

