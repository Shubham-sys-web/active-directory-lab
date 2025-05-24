# active-directory-lab setup
# **Active Directory | Lab Setup**

![](https://miro.medium.com/v2/resize:fit:700/1*08cfxNKKPSOFWchKxE0RSA.png)

**Title: Build an Active Directory Lab at Home Using VirtualBox | 1000+ Users with PowerShell**

## **IntroductionBriefly introduce the goal:**

“In this post, I will walk you through setting up an Active Directory lab on your local machine using VirtualBox, Windows Server 2019, and Windows 10. This setup simulates a production network environment and is ideal for practicing system administration skills like DHCP, NAT, DNS, and user creation via PowerShell.”

**Step 1: Tools Required**

. Oracle Virtual Box

. Windows Server 2019 ISO

. Windows 10 ISO

. Internet connection

. (Optional) PowerShell script for user creation

> Download Link Below required things;
> 
> 
> ***Video Link:** https://www.youtube.com/watch?v=MHsI8hJmggI&t=1s*
> 
> ***Oracle VirtualBox:** https://www.virtualbox.org/wiki/Downloads*
> 
> ***Server 2019 ISO:** https://www.microsoft.com/en-us/evalcenter/download-windows-server-2019*
> 
> ***Windows 10 ISO :** https://www.microsoft.com/en-us/software-download/windows10*
> 
> ***Create Account Powershell Scripts:** https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbmRQRmV6WHpnMWJiVVZwR2dGSWRPelk1eFZqUXxBQ3Jtc0ttTk1tdmhWU0Y1cmZYaTNDUDdvVFF5UVRRV0pZRzVPN2IxVHRyQlBQdi1GZzNQTVg2clFXOUdDOE1RS2ZOWDl2SEpxNmNsaHlkTVFJME9XTkpVdXF2aWxsY1FkcENnWExpeU9MWlFtdklJakh2U3FJVQ&q=https%3A%2F%2Fgithub.com%2Fjoshmadakor1%2FAD_PS%2Farchive%2Frefs%2Fheads%2Fmaster.zip&v=MHsI8hJmggI*
> 

**Step 2: Virtual Network Design (With Diagram)**

First we setup Our DC Server 2019 according to Diagram

Click on new to create the Server 2019 Computer

**Name:** Dc

![](https://miro.medium.com/v2/resize:fit:700/1*kf5kEECapXw1gPqzzNrn6g.png)

**Click on Settings; setup according to my diagram**

![](https://miro.medium.com/v2/resize:fit:700/1*r3mu6eyN5GR-iEs-wIrb1Q.png)

Bi directional it means you can control v like your actual computer and the virtual machine and drag and drop bi-directional means you can drag files like from your desktop from virtual machine it’s pretty easy.

![](https://miro.medium.com/v2/resize:fit:700/1*7Q2GKBr4JIMBFdGn5NzhOA.png)

Setup your CPU according to your PC

![](https://miro.medium.com/v2/resize:fit:700/1*K5NGcUAeG5r7jdGyEp75cw.png)

Set Processor

![](https://miro.medium.com/v2/resize:fit:700/1*-7HhTnUJs96lwmJSceRwnw.png)

**Adapter1:** Here Nat connect to Our House Internet

![](https://miro.medium.com/v2/resize:fit:700/1*eicOeWqEfQAMzFf1yccwIw.png)

**Adapter2:** This is my Internal Network

![](https://miro.medium.com/v2/resize:fit:700/1*mGP1gbOpkNTnj2cHYuI1hA.png)

Double Click on this DC to start our 2019 server

![](https://miro.medium.com/v2/resize:fit:700/1*udUpqXdV1g_FlLDS8v9IBw.png)

Select file from our Desktop 2019 sever Iso

![](https://miro.medium.com/v2/resize:fit:700/1*U2nets1gp-gVmywbJ1RoPQ.png)

Click on next

![](https://miro.medium.com/v2/resize:fit:700/1*EuzESSdVtpNy1Ds2zqhykg.png)

Click on install now

![](https://miro.medium.com/v2/resize:fit:700/1*zk-ihTV1UCrOJHz_pZ8iwg.png)

select according to diagram

![](https://miro.medium.com/v2/resize:fit:700/1*8ZMWVTkocVzxsmpGxVm4vA.png)

Click on next

![](https://miro.medium.com/v2/resize:fit:697/1*S_gjHd04xgcr-UMbmY8lUw.png)

select according to diagram

![](https://miro.medium.com/v2/resize:fit:700/1*XNZEhl3ZBdZl2Ki-z61kpQ.png)

Click on next

![](https://miro.medium.com/v2/resize:fit:650/1*cMPLecPrygTz30bbEhaAOQ.png)

It takes some time to setup

![](https://miro.medium.com/v2/resize:fit:700/1*bIRA3Fjq-OoE8aSSMZiJjQ.png)

Don’t click

![](https://miro.medium.com/v2/resize:fit:700/1*nT4eGda8R-16ct-zxaVNyA.png)

Set Password according to you

![](https://miro.medium.com/v2/resize:fit:700/1*ktRdh9M5DS8BeT6mK4eHYg.png)

Click on : Input to unlock

![](https://miro.medium.com/v2/resize:fit:700/1*r-CMwiu4KRxiiZgCfbXr6w.png)

Select Insert Ctrl+Alt+Del

![](https://miro.medium.com/v2/resize:fit:700/1*B_JklRf0uBITkVlK-IUxSQ.png)

Login with password

![](https://miro.medium.com/v2/resize:fit:700/1*FPbpF-nSJs4iLhnfHl5-sg.png)

This is our Interface

![](https://miro.medium.com/v2/resize:fit:700/1*Hb7N98lhoLhcirlwoA_rgw.png)

Go to the Devices up here select according to the diagram and close it

![](https://miro.medium.com/v2/resize:fit:700/1*Ufhvt9xgZL3xGj34krP7Fg.png)

Go to the PC double click according to the diagram

![](https://miro.medium.com/v2/resize:fit:700/1*fz4LhOH_Zx7zAYRyRLH69w.png)

Select according to the diagram

![](https://miro.medium.com/v2/resize:fit:700/1*MXqkNEwkFuGlYg1TpTkyJg.png)

click on next

![](https://miro.medium.com/v2/resize:fit:700/1*_yzCiuzy3Z1GvKPnywxlzw.png)

Click on next

![](https://miro.medium.com/v2/resize:fit:700/1*0rTiQ8OsNg6YNg7oYFX5wA.png)

Click on install

![](https://miro.medium.com/v2/resize:fit:700/1*8jZhBfaiN_OC1yOtExF82A.png)

Complete the installing wait

![](https://miro.medium.com/v2/resize:fit:700/1*l-oN0s4YbLrMryLiXFCSqA.png)

Click on Finish

![](https://miro.medium.com/v2/resize:fit:700/1*aiK61RvVMvazGLReamNHCA.png)

Click on windows Icon

![](https://miro.medium.com/v2/resize:fit:644/1*W_di07ZW4poIq0HiOc5QNA.png)

Restart your PC and Login

![](https://miro.medium.com/v2/resize:fit:439/1*wZFlUQCNrkzzOt31FPjbdQ.png)

**Step 2: Virtual Network Design (With Diagram)**

![](https://miro.medium.com/v2/resize:fit:591/1*3tG8CVc7PvCi0XRz-SFfwA.png)

**Explain the diagram in parts:**

> DC (Server19) has 2 NICs (Internet & Internal)
> 
> 
> ***Client1 (Win10) gets IP from DC’s DHCP***
> 
> ***VMware/VirtualBox Internal Network for isolation***
> 
> ***IP settings and DHCP scope***
> 

## **Step 3: Creating the Domain Controller VMCreate a new VM in VirtualBox.**

Install Windows Server 2019.

. Attach 2 network adapters:

. Adapter 1 = Bridged/Host-only (for Internet)

. Adapter 2 = Internal Network (for lab)

. Configure static IP for Internal NIC:

IP: 172.16.0.1, Mask: 255.255.255.0, DNS: 127.0.0.1

Setup According to our Diagram

![](https://miro.medium.com/v2/resize:fit:700/1*mHICoL_hJcMUfFZHaSq1pw.png)

Click on change adapter options

![](https://miro.medium.com/v2/resize:fit:700/1*MVKtCe9FDuBDcniNFReyVw.png)

Right Click choose rename

check to both right click and see status

> Ethernet1 : home ip adress -10.10..x.x
> 
> 
> ***ethernet 2 is : DHCP server — 169.154.x.x***
> 

![](https://miro.medium.com/v2/resize:fit:700/1*137hb61dwMgv4zE_ONUCDQ.png)

Change the name

> First: Internet
> 
> 
> ***Second: Internal***
> 

![](https://miro.medium.com/v2/resize:fit:700/1*TRzvxXOK1EJx3Bu868qsVQ.png)

## **Here I forget to assign IP LOL**

First change the name goto the system

![](https://miro.medium.com/v2/resize:fit:700/1*6bW3OW2MCBRgmmIikKlvhw.png)

Restart the server

![](https://miro.medium.com/v2/resize:fit:700/1*TfHSYYwQ5h-UFIhbkwB-9Q.png)

Again do same thing to assign IP

![](https://miro.medium.com/v2/resize:fit:384/1*oCD7TYX2Xb4DmvoWX-gz3Q.png)

Select according to the diagram

![](https://miro.medium.com/v2/resize:fit:581/1*xGi_DTHO0jubB21YADvTPw.png)

Check

![](https://miro.medium.com/v2/resize:fit:597/1*wyQmwd2rdHz_MSL-7hoNaQ.png)

Click on IPv4

![](https://miro.medium.com/v2/resize:fit:353/1*lnVUHxPNGVYJxl78sms0zg.png)

Set IP according to the diagram

![](https://miro.medium.com/v2/resize:fit:411/1*J2LD9INA-kIMH_DMchDhmg.png)

We are Going to install active directory domain services that is adds thing and then we are going to create a domain so lets next step

## **Step 4: Install Active Directory & DNSOpen Server Manager > Add Roles and Features**

Select:

. Active Directory Domain Services

. DNS Server

. Promote to Domain Controller:

. Domain name: mydomain.com

**click on Add roles** Ignore Configure this local server in diagram red line is wrong one

![](https://miro.medium.com/v2/resize:fit:700/1*Y4ytA3jxVvDIdfdPoPGZEQ.png)

Choose active directory click on next

![](https://miro.medium.com/v2/resize:fit:552/1*-sZsVqlkBVdrkSxt9A_Taw.png)

Click on next

![](https://miro.medium.com/v2/resize:fit:460/1*-8aVQgZSWpAdotDKNXJVvA.png)

Click on install

![](https://miro.medium.com/v2/resize:fit:700/1*O8ayrrtdoAXNsKNz74s_Hg.png)

click on close

![](https://miro.medium.com/v2/resize:fit:700/1*Tsi3gkIsgTtXMZPzrfOE6Q.png)

Click on Yellow sign

![](https://miro.medium.com/v2/resize:fit:382/1*tQKcJnTd39vhz1uldi-K7w.png)

Click according to the diagram

![](https://miro.medium.com/v2/resize:fit:402/1*ljnFLcCQaACRFB4-9dR3aw.png)

Here I choose to forest to set a domain

![](https://miro.medium.com/v2/resize:fit:700/1*m0YnrLZ_RrfO2FINk36Dhw.png)

Set Password

![](https://miro.medium.com/v2/resize:fit:700/1*PVvRANyU0jc18I5aNN3tlA.png)

Click on next

![](https://miro.medium.com/v2/resize:fit:700/1*1hvVRkHE8jnajHKWG_ek4A.png)

You can see the domain name and click the next

![](https://miro.medium.com/v2/resize:fit:700/1*WiHVaIBpbj48u8QzSd2T1w.png)

click on next

![](https://miro.medium.com/v2/resize:fit:700/1*Bn4qrfoGUohjXefZSX_JKQ.png)

Click on close

![](https://miro.medium.com/v2/resize:fit:700/1*eyEzKC7hWdTwCPqvZAgC7g.png)

you can see the domain name in diagram

![](https://miro.medium.com/v2/resize:fit:700/1*qzoR67nLddwO7bsx0MNSRw.png)

click on start

![](https://miro.medium.com/v2/resize:fit:639/1*Wzfoon2ZSTFyhwUfKg-xdA.png)

click on windows administartive tools choose

Active directory and Users

![](https://miro.medium.com/v2/resize:fit:411/1*2rDHhWNvDr3FJD-DXIpgEw.png)

You can see that

![](https://miro.medium.com/v2/resize:fit:700/1*glTwLJh0gkOCi0MpARS_aw.png)

Right click on my domain-new-Organization unit

![](https://miro.medium.com/v2/resize:fit:700/1*7xsIFk9ScAHwRQxS81DaTA.png)

Set the name _Admins and click Ok

![](https://miro.medium.com/v2/resize:fit:456/1*N3ccjqPkrbQBr5yt9b6z9w.png)

Now Right click on Admins to new Create User

![](https://miro.medium.com/v2/resize:fit:700/1*-1c5bYrcgaMebO0mHe8Nsw.png)

Keep the name according to you I keep my name

![](https://miro.medium.com/v2/resize:fit:433/1*7H8x1GyQRlSpBMLlNN8GCA.png)

set the password and click on password never expires I don’ take risk and click on next

![](https://miro.medium.com/v2/resize:fit:459/1*HmFUDoPi8BMnkFHa644qAQ.png)

Click on finish

![](https://miro.medium.com/v2/resize:fit:434/1*N_Qlh_IKRw7I2IiRDUSXaw.png)

You can see the user name

![](https://miro.medium.com/v2/resize:fit:668/1*sKQXeqwYk1w2m7isAfGbpw.png)

Right click on the name go the properties

![](https://miro.medium.com/v2/resize:fit:573/1*9xpVWfyF5TzHw5qhalFjlA.png)

Set domains Admins name and click on check names and click on ok

![](https://miro.medium.com/v2/resize:fit:477/1*7dkkMNrJ2iW5ZQBruVdiUA.png)

Now You can see this in Diagram to admins domain name

![](https://miro.medium.com/v2/resize:fit:663/1*c82GNE5387HClS2GN9fwjQ.png)

Select according to the diagram and click on ok

![](https://miro.medium.com/v2/resize:fit:406/1*2sQehC4ZbYj2ugZwO8el0w.png)

Click on start then signout to tthe login in next one

![](https://miro.medium.com/v2/resize:fit:384/1*sra__5fVavOsWRtq5dgnJw.png)

and the login mydoamins admin account

![](https://miro.medium.com/v2/resize:fit:679/1*46fDtRKGpEd6IdJif4_UDg.png)

## **Step 5: Configure NAT with RAS (Remote Access)Use Routing and Remote Access (RRAS)**

. Enable NAT

. Configure:

. Internet NIC = Public

. Internal NIC = Private (connected to internal network)

Go to the Server manager to add role

![](https://miro.medium.com/v2/resize:fit:700/1*nl1iDQvU3S5E97iOOHfDEQ.png)

select remote access

![](https://miro.medium.com/v2/resize:fit:700/1*v61Lw6DSzWiie1asG4xiig.png)

click on next

![](https://miro.medium.com/v2/resize:fit:700/1*_0lOIgfX8aLmQ8K4o6LhpQ.png)

choose both and click on next

![](https://miro.medium.com/v2/resize:fit:700/1*vEp6WWG5Cpcyaju59k89GA.png)

click on install

![](https://miro.medium.com/v2/resize:fit:700/1*NZIgarfUKDxytFF9Xs1pXw.png)

click on close

![](https://miro.medium.com/v2/resize:fit:700/1*GaqSfYZobnuBKkm8zBaH1Q.png)

click on tools

![](https://miro.medium.com/v2/resize:fit:700/1*XIOItmpsHhXhx7jc5mpHRg.png)

choose to Routing and Remote access

![](https://miro.medium.com/v2/resize:fit:270/1*vZc4sv5FV1KQ_NzJYULsTQ.png)

You can see this

![](https://miro.medium.com/v2/resize:fit:661/1*WWwJc-2Yx_54uH8bO415Iw.png)

Right click to enable configure and routing and remote access

![](https://miro.medium.com/v2/resize:fit:622/1*SRv2jJvdwV4t5dYCxqOBMg.png)

click on next

![](https://miro.medium.com/v2/resize:fit:555/1*8S_ybaxXX-NtJA0DQEgdYA.png)

choose NAT click on next

![](https://miro.medium.com/v2/resize:fit:562/1*MkUjduD8zq5FbSZDG84lKQ.png)

I don’t now why this did not worked

![](https://miro.medium.com/v2/resize:fit:541/1*8Of9X1G7leNZTF13Xq_r3g.png)

do same thing one more time

![](https://miro.medium.com/v2/resize:fit:700/1*X2PA1V6O6fV9ktwj2N546Q.png)

right click and select

![](https://miro.medium.com/v2/resize:fit:623/1*f9BrQ4bMDY5dCKFJlWmOHQ.png)

select NAT

![](https://miro.medium.com/v2/resize:fit:606/1*9yw7-FQOr6EJGREOIOAQBg.png)

This time Finally worked you can see both network

![](https://miro.medium.com/v2/resize:fit:676/1*02EhACfN7kyM2LrJz9FEFQ.png)

and select Internet click on next

![](https://miro.medium.com/v2/resize:fit:700/1*5tPjb2_5Cdv7TLKgxWsU5w.png)

click on finish

![](https://miro.medium.com/v2/resize:fit:700/1*UEGj6r0207rGJQMhU2nmmw.png)

cut this page

![](https://miro.medium.com/v2/resize:fit:643/1*0KT2ABc58pbDrblU4O85OQ.png)

you can see our all configuration

![](https://miro.medium.com/v2/resize:fit:700/1*U7MNE8Yp02SbmHaF-fzzcw.png)

## **Step 6: Configure DHCPInstall DHCP Server Role**

Create a new scope:

. Range: 172.16.0.100–172.16.0.200

. Subnet Mask: 255.255.255.0

. Gateway: 172.16.0.1

. DNS: 172.16.0.1

Go the server manager and add roles

![](https://miro.medium.com/v2/resize:fit:700/1*cGA4wwH86tYKinWyM33xiA.png)

click on next

![](https://miro.medium.com/v2/resize:fit:700/1*dRQ74t2cBXiEODRL0hW0iA.png)

select DHCP server

![](https://miro.medium.com/v2/resize:fit:700/1*9lohvXKdt61uOfyq9oezZA.png)

click on install

![](https://miro.medium.com/v2/resize:fit:700/1*m8n4wplTrl6cOotTuiUfsg.png)

after complete installation click on close

![](https://miro.medium.com/v2/resize:fit:700/1*C_k8L1CEkOSAwCVWHpZP2w.png)

Go to the Tools Select DHCP

![](https://miro.medium.com/v2/resize:fit:700/1*DA1blBxMFzoj5wsbUEBSuQ.png)

You can see the configuration

![](https://miro.medium.com/v2/resize:fit:700/1*SgHRg82U694lPyATiKGbrw.png)

All thing in diagram

![](https://miro.medium.com/v2/resize:fit:700/1*cSx4CkAEg7czC3ghDhf5zg.png)

Right click on ipv4 go the new scope

![](https://miro.medium.com/v2/resize:fit:700/1*e72z2Ci9K9w2VKE1m_vMgA.png)

click on next

![](https://miro.medium.com/v2/resize:fit:700/1*2oc-13d2MAVUxNnHdHT3oQ.png)

set the ranges between click on next

![](https://miro.medium.com/v2/resize:fit:700/1*ntpWg10biwF0ZyS-Oe2ilA.png)

set according to the diagram all ranges and subnet mask and click on next

![](https://miro.medium.com/v2/resize:fit:527/1*DVUyxYoT0HKQqnEoKbaTjw.png)

we don’t need this click on next

![](https://miro.medium.com/v2/resize:fit:554/1*LN4IGwehevY9OOAeaoM9Pw.png)

set according to you I comfort to select this one because this is lab setup

![](https://miro.medium.com/v2/resize:fit:553/1*UPenymIZoB6e-9n7kGiCVQ.png)

click on next

![](https://miro.medium.com/v2/resize:fit:589/1*V4T6UI98qJhjDOD21kKf2A.png)

select 172.16.0.1 and click next

![](https://miro.medium.com/v2/resize:fit:700/1*BklFe_jpPtaTlbFA0II6Ig.png)

I don’t nee win server click on next

![](https://miro.medium.com/v2/resize:fit:530/1*Rym6B-9RjOnQ8H_4mWZi6g.png)

click on finish

![](https://miro.medium.com/v2/resize:fit:572/1*w7uwtxd0MA74CH6RCsYIVA.png)

Right click refresh this

![](https://miro.medium.com/v2/resize:fit:541/1*Kpyflh5wq1lcTkDOFyfGcw.png)

right click authorize to unauthorize

![](https://miro.medium.com/v2/resize:fit:512/1*gH4D4wSlo4zRiBlTw5Mpog.png)

again right click to refresh

![](https://miro.medium.com/v2/resize:fit:431/1*ZleZ_BIykdNgObihW0wZzw.png)

cut this page

![](https://miro.medium.com/v2/resize:fit:700/1*VB5LE1qAAmPmaXwmb1pg-Q.png)

## **Step 7: PowerShell — Create 1000+ UsersInclude example code:**

click according with diagram

![](https://miro.medium.com/v2/resize:fit:700/1*BaqvGNAyAB-xlc4nxFRq2A.png)

click on enhanced security

![](https://miro.medium.com/v2/resize:fit:700/1*u_Dr-bVfjeXvlqDV-FRfRQ.png)

here I select to off because our explorer give spam then run script to download why i Off this

![](https://miro.medium.com/v2/resize:fit:621/1*YkPBUY_58AcT2RQPu_ZbtQ.png)

go the explorer

![](https://miro.medium.com/v2/resize:fit:700/1*BzIppyrpsDCoNdW0IMmkbg.png)

copy the link and clock on go to the site

![](https://miro.medium.com/v2/resize:fit:700/1*D_AjFGYdCij4aJXwH5RrzQ.png)

click on save — save as a

![](https://miro.medium.com/v2/resize:fit:700/1*MlFCGkWoEpQ_xicogVqf4A.png)

Save in Desktop

![](https://miro.medium.com/v2/resize:fit:700/1*tAMNDsCLgZS_HGUGOrdbzA.png)

Extract all because i have zip file

![](https://miro.medium.com/v2/resize:fit:414/1*BtdK6UEMIRbTacrwrwFnPQ.png)

select folder

![](https://miro.medium.com/v2/resize:fit:666/1*hBgFQZLnTq9SMpXlP5Ys-Q.png)

I edit this file to with my name because already 1000 user have in this list

![](https://miro.medium.com/v2/resize:fit:700/1*DG6zMaSYcv7RYVfR_nKg1g.png)

save this

![](https://miro.medium.com/v2/resize:fit:275/1*qS0soxNXApAFHQJt7oQoTg.png)

Go to the windows power shell select windows powershell ISE

![](https://miro.medium.com/v2/resize:fit:622/1*kUNql4k37IE_PEM_NBt0PQ.png)

click on yes

![](https://miro.medium.com/v2/resize:fit:569/1*Fvy5qWvOzZES-79w89VE4w.png)

this is power shell inter face and click on select files

![](https://miro.medium.com/v2/resize:fit:700/1*jVR2y_gvoTAawzqHJpp-Ng.png)

select one

![](https://miro.medium.com/v2/resize:fit:678/1*uqP7ExAJSzhJEspwdETtIQ.png)

this is our script

![](https://miro.medium.com/v2/resize:fit:700/1*7xc8yDMHRenmZot5BIqztA.png)

run this give unauthorized access because we have not execution policy

![](https://miro.medium.com/v2/resize:fit:700/1*ojAW6ze6TDzC3jRnrOGn0g.png)

set execution policy with this command

> Set ExecutionPolicy Unrestricted
> 

![](https://miro.medium.com/v2/resize:fit:700/1*XETmu8cMLTekAcHAukXoeQ.png)

This is the script

![](https://miro.medium.com/v2/resize:fit:700/1*GyrmzBWO2YtzvR2LhYlIgw.png)

Here Go to first active directory

![](https://miro.medium.com/v2/resize:fit:667/1*JpzyZMG6B2WzbifFk2RKzg.png)

click on mydomain

![](https://miro.medium.com/v2/resize:fit:700/1*DlbX_S380OXqt1EQZTpNIA.png)

see the all available things under mydomain.com

![](https://miro.medium.com/v2/resize:fit:688/1*yeBJbJwcLccUQfrZnjyK3A.png)

right click on mydomain.com

![](https://miro.medium.com/v2/resize:fit:486/1*AlQ9QA-08Z423ZJcos4dnw.png)

uncheck this to accidental deletion

![](https://miro.medium.com/v2/resize:fit:524/1*G_1qY3CQ8vO5M_WYcsJXRQ.png)

![](https://miro.medium.com/v2/resize:fit:457/1*HKydj8zJnmfbpwnJlqaVHQ.png)

go to the the folder where store our username

![](https://miro.medium.com/v2/resize:fit:700/1*rzj8yWl2Ow7y-yH-6dFRKg.png)

run

![](https://miro.medium.com/v2/resize:fit:179/1*mFVE2XipohROgGTNpgfjYw.png)

click on run once

![](https://miro.medium.com/v2/resize:fit:700/1*rHMjMh9k4kENtrbO4qjdCg.png)

here our creating user

![](https://miro.medium.com/v2/resize:fit:550/1*CStvypk_SFAB2iHFeMzIkg.png)

you can see this all use in active directory

![](https://miro.medium.com/v2/resize:fit:573/1*bb6XTuSK1T3MSXoHtmdj3g.png)

right click and click on find

![](https://miro.medium.com/v2/resize:fit:350/1*pHpsgN2cnhLa4GFgflFxIg.png)

click on find now you can see all users

![](https://miro.medium.com/v2/resize:fit:659/1*Aov12Z1sGD9j4rLIHQlsxw.png)

click on both to check account status one is normal one is admin

![](https://miro.medium.com/v2/resize:fit:525/1*igPI9eO7UXSSiG6TAHQs6w.png)

this is normal account

![](https://miro.medium.com/v2/resize:fit:572/1*NqZAsfuZuJMfGMocXHDJZQ.png)

this is admin account

![](https://miro.medium.com/v2/resize:fit:633/1*h085MCyA9YdhmnzmUDMmZg.png)

here below in diagram total no of users

![](https://miro.medium.com/v2/resize:fit:540/1*KlvnbZue24PHSb7P75thwA.png)

## **Step 7: Setup Client1 (Windows 10)Create a new VM with Windows 10 ISO.**

. Use only Internal NIC.

. Start VM; it should get IP from DHCP on DC.

. Join to domain: mydomain.com

click on new

![](https://miro.medium.com/v2/resize:fit:302/1*zo9mtYAe2H82je7l7dMbsQ.png)

set according to the diagram

![](https://miro.medium.com/v2/resize:fit:700/1*cDTc8mK_4gLYisAgqtP8-Q.png)

double click on client1

![](https://miro.medium.com/v2/resize:fit:494/1*Bu7f4QEQ1djDb0tPXknEhw.png)

click on settings

![](https://miro.medium.com/v2/resize:fit:700/1*loLuVEnfh0EjsfLE3npsLA.png)

again set bidirectional to drag on drop

![](https://miro.medium.com/v2/resize:fit:700/1*4vdBxhrxJcwODi1VAQrKjg.png)

set according to your cpu

![](https://miro.medium.com/v2/resize:fit:700/1*m3ebu3ONgQsei5D4B63NMw.png)

Set internal network

![](https://miro.medium.com/v2/resize:fit:700/1*Prj1EYQYiUkM8Hfm_qnG6w.png)

click on select

![](https://miro.medium.com/v2/resize:fit:700/1*Ie4uUdc2qo_0oHqFJmaXCw.png)

select windows 10 ISO

![](https://miro.medium.com/v2/resize:fit:700/1*gc5pJmzSBRKs1cVKh7jbOw.png)

Click on mount and Retry boot

![](https://miro.medium.com/v2/resize:fit:692/1*JXeRYhA3KYkSjhBEguaISw.png)

click on next

![](https://miro.medium.com/v2/resize:fit:700/1*i9PH0SHoqJ3kqx2ZPqMioQ.png)

click on i don’t have product key

![](https://miro.medium.com/v2/resize:fit:700/1*ioPk0gUNk1KWw2UuOgR4ZA.png)

select windows 10 pro

![](https://miro.medium.com/v2/resize:fit:700/1*dyVybxKPcoKGU9KzkxbS2Q.png)

click on next

![](https://miro.medium.com/v2/resize:fit:700/1*tVUphuryiLlLOaoTWbby0A.png)

choose according to diagram

![](https://miro.medium.com/v2/resize:fit:663/1*dGSwdqJfgu7spm3ckwVItw.png)

click on next

![](https://miro.medium.com/v2/resize:fit:651/1*_rCydhhZQBudp5_wdaYaFQ.png)

wait for installing

![](https://miro.medium.com/v2/resize:fit:700/1*1hyUs24ukW6TKLlyAHaeZg.png)

select your region

![](https://miro.medium.com/v2/resize:fit:700/1*YNdM2uKmxczWbqjcE9PEgg.png)

select

![](https://miro.medium.com/v2/resize:fit:700/1*vaLGrpXxv8Fh7M_sGZ6z3w.png)

click on skip

![](https://miro.medium.com/v2/resize:fit:700/1*wdl_Vkw1VyhObY1nPgBLVw.png)

click on i don’t have internet

![](https://miro.medium.com/v2/resize:fit:700/1*Itnxb5VMKIyxNSJSwxIi5w.png)

click on limited setup

![](https://miro.medium.com/v2/resize:fit:700/1*pNvxbwdou48d25h-XY7U6A.png)

give username user

![](https://miro.medium.com/v2/resize:fit:700/1*30mrs3uCYC2H_3VYNrkD-g.png)

don’t fill the password ignore this and click on next logging without password

![](https://miro.medium.com/v2/resize:fit:700/1*_Bq5oPX_U7vY5FWGlxMoLQ.png)

off every thing

![](https://miro.medium.com/v2/resize:fit:700/1*asFiUEyU5aqF09SEDV0ShQ.png)

click on accept

![](https://miro.medium.com/v2/resize:fit:700/1*xrGlwcpgmwQwtkt4nFITFQ.png)

again click on accept

![](https://miro.medium.com/v2/resize:fit:700/1*l4PxmmbW1P_fTJ5Tw7gX5w.png)

don’t click anythings

![](https://miro.medium.com/v2/resize:fit:700/1*MaIJN6l0cK-lVIaPu6VTdg.png)

main interface of windows10

![](https://miro.medium.com/v2/resize:fit:700/1*SB4aDmPRz2gv_v5Pewmycw.png)

search ip address but one this is missing default gateway some reason behind this

![](https://miro.medium.com/v2/resize:fit:700/1*mpkwTH6oKauN9gePKaeXqA.png)

## **This is the Domain Controller**

![](https://miro.medium.com/v2/resize:fit:700/1*rD97XFmbgqOLqc0C1ak5JQ.png)

Go to the tools click on DHCP

![](https://miro.medium.com/v2/resize:fit:700/1*f5BB07YMRvq9UEsiYsuUxA.png)

click on server option and configure options

![](https://miro.medium.com/v2/resize:fit:584/1*X4D6-zDjdPrS6y3GI0rZ-Q.png)

Here I forget this

![](https://miro.medium.com/v2/resize:fit:700/1*goMJDOZccv7ZjFfnPJws0g.png)

select router click on apply

![](https://miro.medium.com/v2/resize:fit:519/1*DceY45Ju4ztlDQLAvfX33Q.png)

click on ok

![](https://miro.medium.com/v2/resize:fit:380/1*6BOg6B4LT_1T0QZXI6gkWw.png)

Right Click on dc.mydomain.com-all task-Restart

![](https://miro.medium.com/v2/resize:fit:604/1*Cgm8MJcpf-teQO0w8TkslQ.png)

wait

![](https://miro.medium.com/v2/resize:fit:510/1*O09K4Seoi0aSBgGStKMRXg.png)

you can see this

![](https://miro.medium.com/v2/resize:fit:700/1*h8wMMg3D6IRJ5TdogHLrNA.png)

again search ip via ipconfig didn’t worked

![](https://miro.medium.com/v2/resize:fit:554/1*51e_jo5O-yYOO8FuMGlxbA.png)

renew ip

![](https://miro.medium.com/v2/resize:fit:554/1*07uhVIZn8px19yrlbM45iQ.png)

this time show our Default gateway

![](https://miro.medium.com/v2/resize:fit:546/1*2MTh6kUlN09lesTDGnTljA.png)

Here ping is worked google.com

![](https://miro.medium.com/v2/resize:fit:526/1*WTuGIQNUQJGU3-hQ46WGxg.png)

and mydomain.com is also working

## **our whole infrastructure is working**

![](https://miro.medium.com/v2/resize:fit:473/1*yk2KgdIKqv8WlFO3N9e-nA.png)

right click on start menu go to the system - click on Rename this Pc (advanced) ignore **red arrow**

![](https://miro.medium.com/v2/resize:fit:637/1*9yyeCdeVhGLL6L4c_ULIxg.png)

Don’t write on Computer discription and click on change

![](https://miro.medium.com/v2/resize:fit:280/1*K3BVlWYzXWCA7t1i--inoA.png)

Change according to the diagram

first computer name and we are also going to try to join the domain at the same time so mydomain.com

![](https://miro.medium.com/v2/resize:fit:630/1*VeLvN3pbotJoqOf7TUWX2Q.png)

and the you need to type a password who is allowed to join this account to the domain and remember we did we created a domain admin account we created two accounts actually we created like our normal account which I don’t think will work so let’s just try it

![](https://miro.medium.com/v2/resize:fit:463/1*0P2oh4oQmzwnnJCnoQBOiQ.png)

Oh actually worked that is cool click on ok

![](https://miro.medium.com/v2/resize:fit:552/1*LTujT3B2zJaVifq2He_40g.png)

click on ok

![](https://miro.medium.com/v2/resize:fit:533/1*s_YqC3XRVziHidKlV2HBtg.png)

restart your pc

![](https://miro.medium.com/v2/resize:fit:384/1*ejKishnc_yHhpkB0hIw_QQ.png)

Here let’s Go back to the DOMAIN CONTROLLER

![](https://miro.medium.com/v2/resize:fit:700/1*wz_cK76xYD-iQouSnroHBw.png)

expand this go the address leases and then we can see in here we have one lease from our client computer so when we created our client computer and like kind of joined it to the network um it reached out to the dhcp server automatically and requested and address and then then the dhcp server gave it address and now we have this lease in here

![](https://miro.medium.com/v2/resize:fit:700/1*M7gu5Tt71GRYFZjT8LYrUw.png)

another thing is let’s go to the active directory users and computers so this is still domain controller . we can see that after we joined this client computer to the domain um like the thing we just did this thing automatically came in here kind of showing that this computer is a member of the domain

![](https://miro.medium.com/v2/resize:fit:691/1*x_ujbX2WCYeTdwlc1_t-Xg.png)

So back to the our **windows 10** machine

![](https://miro.medium.com/v2/resize:fit:700/1*5FCKq9QigsYqzbSIhOoWmQ.png)

so we can login with normal user and password we created click on other user

![](https://miro.medium.com/v2/resize:fit:700/1*PFLU8MRz22YZ7VlWxL7fJQ.png)

wait

![](https://miro.medium.com/v2/resize:fit:700/1*FtCopktBNNmCJCApZy9V1g.png)

Everything is cool

![](https://miro.medium.com/v2/resize:fit:700/1*mjG2UDKu9iJIaBhsle8Kmg.png)

if we go to the command line we say who am i um you can see that you are a member of mydomain and then your username is shubham choudhari mean schoudhari

![](https://miro.medium.com/v2/resize:fit:538/1*JlmGL8A7BRUvzAlHqBGX3A.png)

**Conclusion**

Wrap up:

“With this setup, you now have a fully functional Windows domain environment for testing, learning, and scripting. Perfect for lab practice, especially for certifications or real-world scenarios.”
