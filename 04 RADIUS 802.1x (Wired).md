
<!-- Your monitor number = #$34T# -->

# 💡 Setup RADIUS Server for 802.1x Wired Authentication

### 1. On Networ Policy Server
Drop down `RADIUS Clients and Servers` __[01]__. Then, right-click `RADIUS Clients` __[02]__, `New` __[03]__

<br>

![01-AAA](<img/00 RADIUS-Wired-01.png>)

&nbsp;
---
&nbsp;

### 2. New RADIUS Client
> [!IMPORTANT]
> The RADIUS Client to be configured for this guide, is a CSR1000v with an IP of 208.8.8.11  
>  
> If you are going to use a different RADIUS client, make sure to specify the appropriate IP address.

<br>

- Friendly name: `CSR1000v` __[04]__  
- Address: `208.8.8.11` __[05]__
- Shared Secret: `C1sc0123` __[06]__

<br>

Then, select `OK` __[07]__

![02-AAA](<img/00 RADIUS-Wired-02.png>)

&nbsp;
---
&nbsp;

### 3. Create New Network Policies
Drop down `Policies` __[08]__. Then, right-click `Network Policies` __[09]__, select `New` __[10]__.

<br>

![03-AAA](<img/00 RADIUS-Wired-03.png>)

&nbsp;
---
&nbsp;

### 4. Specify Network Policy Name and Connection Type
Specify a policy name, `Win-RADPolicy` __[11]__. Then, `Next` __[12]__

<br>

![04-AAA](<img/00 RADIUS-Wired-04.png>)

&nbsp;
---
&nbsp;

### 5. Specify Conditions
Select `Add...` __[13]__

<br>

![05-AAA](<img/00 RADIUS-Wired-05.png>)

&nbsp;
---
&nbsp;

### 6. Select Condition
Select `Windows Groups` __[14]__, then `Add` __[15]__

<br>

![06-AAA](<img/00 RADIUS-Wired-06.png>)

&nbsp;
---
&nbsp;

### 7. Windows Groups
Select, `Add Groups...` __[16]__.  

<br>

![07-AAA](<img/00 RADIUS-Wired-07.png>)

&nbsp;
---
&nbsp;

### 8. Add User Groups
Type `Do` __[17]__, then `Check Names` __[18]__. On, the Multiple Names Found window, select `Domain Users` __[19]__. Then, `OK` __[20]__.

<br>

![08-AAA](<img/00 RADIUS-Wired-08.png>)

&nbsp;
---
&nbsp;

### 9. Select Group
Then, select `OK` __[21]__

<br>

![09-AAA](<img/00 RADIUS-Wired-09.png>)

&nbsp;
---
&nbsp;

### 10. Windows Groups
Confirm the selected groups `OK` __[22]__

<br>

![10-AAA](<img/00 RADIUS-Wired-10.png>)

<br>
<br>

![10-AAA](<img/00 RADIUS-Wired-11.png>)

<br>

Then, `Next` __[23]__

&nbsp;
---
&nbsp;

### 11. Specify Access Permission
Leave as Default, select `Next` __[24]__

<br>

![13-AAA](<img/00 RADIUS-Wired-12.png>)

&nbsp;
---
&nbsp;

### 12. Configure Authentication Methods
Disable all Microsoft Authentication Methods, and select only `Unencrypted authentication (PAP, SPAP)` __[25]__  
Then, select `Next` __[26]__  

<br>

![14-AAA](<img/00 RADIUS-Wired-13.png>)

&nbsp;
---
&nbsp;

### 13. Confirm Request Policy
Windows simply throw a warning, ignore it. Select `No` __[27]__

<br>

![15-AAA](<img/00 RADIUS-Wired-14.png>)

&nbsp;
---
&nbsp;

### 14. Configure Constraints
Select __[28]__

<br>

![16-AAA](<img/00 RADIUS-Wired-15.png>)

&nbsp;
---
&nbsp;

### 15. Configure Settings
Under RADIUS Attributes, select `Standard` __[29]__.  
Select `Framed-Protocol` __[30]__, then, `Remove` __[31]__

<br>

![17-AAA](<img/00 RADIUS-Wired-16.png>)

&nbsp;
---
&nbsp;

### 16. Add Attributes
Select, 'Service-Type' __[32]__. Then, `Edit` __[33]__

<br>

![18-AAA](<img/00 RADIUS-Wired-17.png>)

&nbsp;
---
&nbsp;

### 17. Attribute Information
Under Attribute Value, select 'Others' __[34]__. Then, specify 'Login` __[35]__, then `OK` __[36]__. 

<br>

![19-AAA](<img/00 RADIUS-Wired-18.png>)

&nbsp;
---
&nbsp;

### 18. Vendor Specification
Select, `Vendor Specific` __[37]__ . Then, `Add...` __[38]__
 
<br>

![20-AAA](<img/00 RADIUS-Wired-19.png>)

&nbsp;
---
&nbsp;

### 19. Add Vendor Specific Attribute
For Vendor, select `Cisco` __[39]__. Select `Cisco-AV-Pair` __[40]__. Then, `Add...` __[41]__

<br>

![21-AAA](<img/00 RADIUS-Wired-20.png>)

&nbsp;
---
&nbsp;

### 20. Attribute Information
On, Attribute Value, enter the string: `shell:priv-lvl=15` __[42]__. Then, `OK` __[43]__.

<br>

![22-AAA](<img/00 RADIUS-Wired-21.png>)

&nbsp;
---
&nbsp;

### 21. Confirm Attribute Information
Select, `OK` __[44]__. Then, `Close` __[45]__.

<br>

![23-AAA](<img/00 RADIUS-Wired-22.png>)

&nbsp;
---
&nbsp;

### 22. Encryption
Select `Encryption` __[46]__. Then, uncheck the other encryption and select only `No encryption` __[47]__  
Then, select `Next` __[48]__

<br>

![24-AAA](<img/00 RADIUS-Wired-23.png>)

&nbsp;
---
&nbsp;

### 23. Confirm Network Policy
Finally, `Finish` __[49]__

<br>

![25-AAA](<img/00 RADIUS-Wired-24.png>)

&nbsp;
---
&nbsp;

### 24. Set Policy
Right-click on the recently created policy, `Win-RADPolicy` __[50]__. Then, select `Move Up` __[51]__  
Keep, moving the policy until it's at the very top.  

<br>

![26-AAA](<img/00 RADIUS-Wired-25.png>)

&nbsp;
---
&nbsp;

### 25. Confirmation

![27-AAA](<img/00 RADIUS-Wired-26.png>)
