
<!-- Your monitor number = #$34T# -->

# 💡 Install Certificate Services

### 1. On Server Manager
Go to Manage > `Add Roles and Features` __[01]__

<br>

![01-CA](<img/00 AD-01.png>)

&nbsp;
---
&nbsp;

### 2. Before You Begin
Leave the initial prompt to defaults. Select `Next` __[02]__

<br>

![02-CA](<img/00 AD-02.png>)

&nbsp;
---
&nbsp;

### 3. Installation Type.
Select `Next` __[03]__ again.

<br>

![03-CA](<img/00 AD-03.png>)

&nbsp;
---
&nbsp;

### 4. Destination Server
Select `Next` __[04]__
> [!IMPORTANT]
> The destination server is itself. The initial configuration is based on the Windows Server 2022 setup.

<br>

![04-CA](<img/00 AD-04.png>)

&nbsp;
---
&nbsp;

### 5. Select Server Roles
Select `Active Directory Certificate Services` __[05]__
<br>

![05-CA](<img/00 CA-01.png>)

&nbsp;
---
&nbsp;

### 6. Add Features
Select `Add Features` __[06]__
<br>

![06-CA](<img/00 CA-02.png>)

&nbsp;
---
&nbsp;

### 7. Server Roles
Select `Next` __[07]__
<br>

![07-CA](<img/00 CA-03.png>)

&nbsp;
---
&nbsp;

### 8. Select Features
Select `Next` __[08]__
<br>

![08-CA](<img/00 CA-04.png>)

&nbsp;
---
&nbsp;

### 9. Certificate Services Configuration
Select `Next` __[09]__
<br>

![09-CA](<img/00 CA-05.png>)

&nbsp;
---
&nbsp;

### 10. Role Services for Certificate Services
Leave as default. Select `Next` __[10]__
<br>

![10-CA](<img/00 CA-06.png>)

&nbsp;
---
&nbsp;

### 11. Confirm Installation
Select `Install` __[11]__
<br>

![11-CA](<img/00 CA-07.png>)

&nbsp;
---
&nbsp;

### 12. Configure Certificate Services
After the installation is complete, setup AD CS by selecting `Configure Active Directory Certificate Services on the destination server` __[12]__
<br>

![12-CA](<img/00 CA-08.png>)

&nbsp;
---
&nbsp;

### 13. Credentials
Select `Next` __[13]__
<br>

![13-CA](<img/00 CA-09.png>)

&nbsp;
---
&nbsp;

### 14. Configure Role Services
Select `Certificate Authority` __[14]__. Then, select `Next` __[15]__
<br>

![14-CA](<img/00 CA-10.png>)

&nbsp;
---
&nbsp;

### 15. Setup Type
Select `Enterprise CA` __[16]__. Then, select `Next` __[17]__
<br>

![15-CA](<img/00 CA-11.png>)

&nbsp;
---
&nbsp;

### 16. CA Type
Select `Root CA` __[18]__. Then, select `Next` __[19]__
<br>

![16-CA](<img/00 CA-12.png>)

&nbsp;
---
