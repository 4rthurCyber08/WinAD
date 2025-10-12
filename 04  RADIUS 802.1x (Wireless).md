
<!-- Your monitor number = #$34T# -->

# 💡 Setup RADIUS Server for 802.1x Wireless Authentication

### 1. On Server Manager
Go to Manage > `Network Policy Server` __[01]__

<br>

![01-AAA](<img/AAA-01.png>)

&nbsp;
---
&nbsp;


### 2. Standard Configuration
On Network Policy Server, select `NPS(Local)` __[02]__. Then, on the drop down, select `RADIUS server for 802.1X Wireless or Wired Connections` __[03]__. Then, `Configure VPN or Dial-Up` __[04]__

<br>

![02-AAA](<img/AAA-02.png>)

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

### 8. Select Group
Enter the first 2 letters of the specified User Group: `Do` __[16]__. Then, in case there is a lot of user groups or you don't remember them, you can select `Check Names` __[17]__

<br>

![09-AAA](<img/AAA-09.png>)

&nbsp;
---
&nbsp;

### 9. Find Names
Select `Domain Users` __[18]__. Then, `OK` __[19]__

<br>

![10-AAA](<img/AAA-10.png>)

&nbsp;
---
&nbsp;
