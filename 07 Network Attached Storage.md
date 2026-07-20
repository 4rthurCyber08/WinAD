
<!-- Your monitor number = #$34T# -->

# 💡 Network Attached Storage

### 1. Install the ff
- DFS Namespaces
- Data Deduplication
- DFS Replication
- File Server Resource Manager


&nbsp;
---
&nbsp;


### 2. Create Shares Folders
- C:\Shares
- C:\Shares\NOC
- C:\Shares\SOC
- C:\Shares\FIN
- C:\Shares\Makati Documents


&nbsp;
---
&nbsp;


### 3. Folder Sharing & Permissions
Share the C:\Shares on Server Manager

Permissions:
- SYSTEM
- Administrators
- Creator Owner
- MKT-Branch

Applies to: This Folder Only


&nbsp;
---
&nbsp;


### 4. OU Security Permissions
- NOC
  - Permissions: 
    - SYSTEM
	- Administrators
	- Creator Owner
	- LGNOC


- SOC
  - Permissions: 
    - SYSTEM
	- Administrators
	- Creator Owner
	- LGSOC


- FIN
  - Permissions: 
    - SYSTEM
	- Administrators
	- Creator Owner
	- LGFIN


<br>


New DFS Namespaces
- Server: iam-92
  Namespace Name: NOC-FILES

- Server: iam-92
  Namespace Name: SOC-FILES

- Server: iam-92
  Namespace Name: FIN-FILES


&nbsp;
---
&nbsp;


### 5. Access Network Files based on User Accounts

!@cmd - Real WinServer
net use h: \\192.168.103.8\Shares /user:ac C1sc0123
net use h: /delete
