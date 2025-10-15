
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

### 3. 802.1X Connection Type
Select `Secure Wireless Connections` __[05]__. Then, `Next` __[06]__

<br>

![03-AAA](<img/AAA-03.png>)

&nbsp;
---
&nbsp;

### 4. Specify 802.1X Switches
`Add...` __[07]__ a RADIUS client.

<br>

![04-AAA](<img/AAA-04.png>)

&nbsp;
---
&nbsp;

### 5. New RADIUS Client
> [!IMPORTANT]
> The RADIUS Client to be configured for this guide, is a C9800 WLC with an IP of 10.92.1.7
>  
> If you are going to use a different RADIUS client, make sure to specify the appropriate IP address.

<br>

- Friendly name: `C9800-WLC` __[08]__  
- Address: `10.#$34T#.1.7` __[09]__
- Shared Secret: `C1sc0123` __[10]__

<br>

Then, select `OK` __[11]__

<br>

![05-AAA](<img/AAA-05.png>)

&nbsp;
---
&nbsp;

### 6. Finalize 802.1X clients
Select `Next` __[12]__

<br>

![06-AAA](<img/AAA-06.png>)

&nbsp;
---
&nbsp;

### 7. Configure an Authentication Method
Select `Microsoft: Protected EAP (PEAP)` __[13]__.  

<br>

Then, select `Next` __[14]__

<br>

![07-AAA](<img/AAA-07.png>)

&nbsp;
---
&nbsp;

### 8. Add User Groups
`Add...` __[15]__

<br>

![08-AAA](<img/AAA-08.png>)

&nbsp;
---
&nbsp;

### 9. Select Group
Enter the first 2 letters of the specified User Group: `Do` __[16]__. Then, in case there is a lot of user groups or you don't remember them, you can select `Check Names` __[17]__

<br>

![09-AAA](<img/AAA-09.png>)

&nbsp;
---
&nbsp;

### 10. Find Names
Select `Domain Users` __[18]__. Then, `OK` __[19]__

<br>

![10-AAA](<img/AAA-10.png>)

&nbsp;
---
&nbsp;

### 11. Confirm Group Selection
Verify if `Domain Users` __[20]__ is now listed. Then, `OK` __[21]__

<br>

![11-AAA](<img/AAA-11.png>)

<br>
<br>

Then `Next` __[22]__

<br>

![12-AAA](<img/AAA-12.png>)

&nbsp;
---
&nbsp;

### 12. Traffic Controls
Leave as Default, select `Next` __[23]__

<br>

![13-AAA](<img/AAA-13.png>)

&nbsp;
---
&nbsp;

### 13. Confirm Configurations
Finally, select `Finish` __[24]__

<br>

![14-AAA](<img/AAA-14.png>)

