![](http://i.imgur.com/pm6WkXO.jpg)

###SRI LANKA INSTITUTE OF INFORMATION TECHNOLOGY
##  ##

#####Enterprise Standards and Best Practices for IT Infrastructure

#####4th Year 2nd Semester 2014

#######Name: Gunasinghe S.U <br>
#######SLIIT ID: IT13022570 <br>
#######Practical Session: WD Friday<br>
#######Practical Number: Lab 4

--------------------------------------------------------------------------------

###Getting started with ESXi 5<br>
01.First need to add a new virtual machine on the top of current Operating System.<br>
02.Then we need to install the baremetal installer. 

![](http://i.imgur.com/xT7Redd.png)<br>

03.Then need to install the baremetal OS.<br>
   Browse the baremetal installer to the installer disk image file.
![](http://i.imgur.com/5zQSoqN.png)<br><br>


04.Choose Store virtual disk as a single file. Click on next.
![](http://i.imgur.com/VQtdJ9U.png)<br>

05.Then you have to start the ESXi 5 installer. Then the installer gives you the details the status of each file that need to be loaded.

![](http://i.imgur.com/4qYDIzl.png)<br>

06.Here shows some information about the server, including the processor type and system RAM.
![](http://i.imgur.com/aYmyGNq.png)<br>

07.Then appears a dialog Welcome to the VM war e ESXI Installation and to continue with the installation, press Enter on the keyboard.
![](http://i.imgur.com/4uYM0yC.png)<br>

08.Then you can see the End user  license  agreement to accept the agreement press F11
![](http://i.imgur.com/6wvpZa1.png)<br>

09.Then we have to choose a location to install ESXi 5.<br>
Then press Enter. 
![](http://i.imgur.com/013SaH6.png)<br>

10.Then provide a password for the root user account.<br>
Press Enter
![](http://i.imgur.com/utLlHT7.png)<br>

11.Then the ESXi installer scans the system to get additional information. 
![](http://i.imgur.com/cGUhHJ6.png)<br>

12.Then ask to confirm install. Press F11 button to install.
![](http://i.imgur.com/V7jLMUf.png)<br><br>

13.Installation status.
![](http://i.imgur.com/V6M7WcM.png)<br> 

14.Then the installation complete dialog box will be shown. To Reboot, press Enter.
![](http://i.imgur.com/DitzCOp.png)<br><br>

15.Get the IP address.
![](http://i.imgur.com/tELxdZx.png)
<br><br>
![](http://i.imgur.com/GiOgwYa.png)<br>

16.Get the command prompt and type ping 192.168.44.128
![](http://i.imgur.com/UZKATGc.png)<br>

###Install  the  vSphere  Client
01.Get the IP address and search in a web browser.There you can download the vSphere client.
![](http://i.imgur.com/7occJbN.png)<br><br>

02.Execute the client software installation routine<br>
03.You have installed the hyper visor – ESXi5 and a management tool – v Sphere Client.
Start the vSphere client. Then provide the IP address for your ESX i5 host and also provide the root user name and password that you specified during the setup of your server.
![](http://i.imgur.com/uL7O8pq.png)<br>

04.After login to the VMware vSphere client you can get a security warning.This is basically telling you that the SSL certificate being used by the ESXi host cannot be trusted. Since you just installed the ESXi server, you can click on the ignore button.
![](http://i.imgur.com/aNILIV7.png)<br>
05.This is the interface then you get.
![](http://i.imgur.com/2ypgNER.png)<br>
06.Then click on the Inventory .Then there are several tabs. Getting started tab is in this interface.
![](http://i.imgur.com/fyIuQAC.png)<br><br>
![](http://i.imgur.com/t9r7NG4.png)
<br><br>
![](http://i.imgur.com/o2IwwF0.png)<br><br>
![](http://i.imgur.com/3Qe5YYM.png)
<br><br>
![](http://i.imgur.com/3fQghwb.png)<br><br>
![](http://i.imgur.com/Y0QNvJx.png)
<br><br>
![](http://i.imgur.com/R6v4MHc.png)
<br><br>
![](http://i.imgur.com/zuOqOYE.png)<br><br>
![](http://i.imgur.com/0Tk0Wh6.png)<br>

07.In summary tab, there is a resource called storage. Right click on the database and select Browse data store.
<br>
08.In data store browser, there is an icon in navigation pane.(4th icon).Click on that icon and select Upload File.
![](http://i.imgur.com/Uzjvdsq.png)<br>

09.Select the available Linux /windows image file. Here upload the kali Linux  image file to the data store.
![](http://i.imgur.com/FcSzcbJ.png)<br><br>
![](http://i.imgur.com/YxSnsJo.png)
<br>
10.Then right click on the IP address shown in the top left corner. Select new virtual Machine.<br>
11.Then create a new virtual machine using usual steps. Then choose Typical. Then Click next.
![](http://i.imgur.com/tm7S3Ti.png)<br>

12.Give a specific name for this virtual machine.
![](http://i.imgur.com/Qpub0EG.png)<br>

13.Then choose the data store. Then click next.
![](http://i.imgur.com/LvDIcH8.png)<br>

14.Specify the guest operating system to use with this virtual machine. Here choose the Linux because before chose the kali Linux image file. Then click next
![](http://i.imgur.com/nEt5StT.png)<br>

15.Specify the Adapter as E1000 and tick the Connect at power on. The E1000 is an emulated version of the Intel 82545EM Gigabit Ethernet adapter. Not all guest operating systems include support for this adapter.
![](http://i.imgur.com/yXd5uNl.png)<br>

16.Specify the virtual disk size and provisioning policy. As the Provision here selected the Thin provision. Then click next.
![](http://i.imgur.com/DiTfQnP.png)<br><br>
![](http://i.imgur.com/LJkTpSS.png)<br>

17.Then you can see the kali_linux instance has been created under the IP address top left corner.Right click on that instance and go to Edit Settings.<br>
18.Then click on the CD/DVD drive 1.In the right side you can see the Data store  ISO file .Tick on that and brow se the kali Linux image file  inside the data store 1.
![](http://i.imgur.com/5I7xJID.png)<br>
![](http://i.imgur.com/Z3M2zbW.png)<br>
![](http://i.imgur.com/pUYS1rR.png)<br>

19.Then go to Getting started tab and Start the  virtual machine .Then go to Console  tab. Then you can see the kali_linux  virtual machine is getting started
![](http://i.imgur.com/T47tCmS.png)<br><br>
![](http://i.imgur.com/YuJ7C3D.png)<br><br>
![](http://i.imgur.com/pct7Zaj.jpg)


