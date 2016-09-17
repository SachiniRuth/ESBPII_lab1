![](http://i.imgur.com/EnnWvFP.jpg)



####SRI LANKA INSTITUTE OF INFORMATION TECHNOLOGY

#####Enterprise Standards and Best Practices for IT Infrastructure
---------------------------------------------------------------------------------

4th Year 2nd Semester 2016<br>
Name: Gunasinghe S.U<br>
SLIIT ID: IT13022570<br>
Practical Session: WD Friday<br>
Practical : V motion <br>


---------------------------------------------------------------------------------

###vMotion<br>
virtual machine can move from one physical server to another while it's running without any downtime to end users. (running virtual machine moves
from one host to another)<br>

####1.vMotion Requirements<br>
- virtual machine must not have a connection to a virtual device such as a CD-ROM with a logical image mounted. if they are connected to a
host, that will block the Motion migration. solution-store those devices in a shared data store.<br>
- need to make sure to have storage between ESXi servers-iSCSI ,CF, NFS(shared storage) so the both hosts can see the vm files from the shared storage.<br>
- each host must have the Gigabit Ethernet network connection.<br>
- host must be plugged into the same physical network.<br>
- vMotion works with standard switches or destributed virtual switches.<br>
- should have CPU  compatibility. otherw ise w e can' t do the migration. follow ing is happen w hen there is no CPU  compatibility. it says that the
vMotion is blocking because, there ,is a CD-ROM is attatched to the data store that is not accessible to the host.<br>

####2.Benefits of vMotion.<br>
- Automatically optimize and allocate entire pools of resources.<br>

By having all your server and/or desktops virtualized you can move VM’s from one physical host to another, which is done rapidly over a high speed network connection, the original host and destination host stay in sync until the transfer it complete leaving the user unaware of the move.
This allow s network administrators to easily select resource pools to assign to the different VMs.<br>

- minimiz e the scheduled downtime.<br>

only have to move the VM to another physical host, creating zero downtime for the users and allowing administrators to perform maintenance at any time.<br>

####3.How to configure  hosts to do the vMotion.<br>

![](http://i.imgur.com/ZNYoHSG.png)<br>

Now we look at the tab Configuration-> Networking<br>

![](http://i.imgur.com/ZZhj6On.jpg)<br>

Click on Add Networking to create the vSwitch.<br>

![](http://i.imgur.com/hw9Vg4f.jpg)<br>

Select VMKernel and click on Next.<br>

![](http://i.imgur.com/wQEelkf.jpg)<br>

Making a network card or cards that have connected from one server to another (in our case vmnic9) And click on Next.<br>

![](http://i.imgur.com/G3VRAeo.png)<br>

We set Use this port group for vMotion.<br>

We wrote a Label Network different if you want (optional) and click on Next. We for example we put Vmotion.<br>

![](http://i.imgur.com/wCEkF1z.png)<br>

We set Use the following IP settings:<br>

IP Address: 50.50.50.1<br>
Subnet Mask: 255.255.255.252 (Since we will use only 2 ip's).<br>
Click on Next.<br>

![](http://i.imgur.com/GITzkHz.png)<br>

Click on Finish.<br>

![](http://i.imgur.com/lGj88dP.png)<br>

We found that they have created a new virtual switch with Vmotion.<br>

We connect to another server involved.<br>

We select the tab Configuration-> Network Adapters and we see that we have visibility of the new connections.<br>

![](http://i.imgur.com/7Xpb1bB.png)<br>

Now we look at the tab Configuration-> Networking<br>

![](http://i.imgur.com/AHzUhGd.png)<br>

Click on Add Networking to create the vSwitch.<br>

![](http://i.imgur.com/quEa6NP.png)<br>

Select VMKernel and click on Next.<br>

![](http://i.imgur.com/8WLy3mJ.png)<br>

Making a network card or cards that have connected from one server to another (in our case vmnic9) And click on Next.<br>

![](http://i.imgur.com/IZkLm83.png)<br>

We set Use this port group for VMotion.<br>

We wrote a Label Network different if you want (optional) and click on Next. We for example we put Vmotion.<br>

![](http://i.imgur.com/sBTz5QF.png)<br>

We set Use the following IP settings:<br>

IP Address: 50.50.50.2 (This ip must be different from the server that we configured earlier 1).<br>

Subnet Mask: 255.255.255.252 (Since we will use only 2 ip's).<br>

Click on Next.<br>

![](http://i.imgur.com/OVhetVK.png)<br>

Click on Finish.<br>
And now what we will do to ensure that the entire system is working properly migrate a VM from one ESXi to the other using Vmotion functionality you just configured.<br>
We press the right mouse button on a virtual machine.<br>

![](http://i.imgur.com/q1E4aVc.png)<br>

Click on Migrate.<br>

![](http://i.imgur.com/CVpemoA.png)<br>

Click on Next.<br>

![](http://i.imgur.com/xOTMcWm.png)<br>

Select the target server where we will move the virtual machine.<br>

Click on Next.<br>

![](http://i.imgur.com/D4vJooV.png)<br>

Click on Next.<br>

![](http://i.imgur.com/R6SGyWx.png)<br>

Click on Finish to start the migration.<br>

![](http://i.imgur.com/YEQT7kF.png)<br>

Perfect the system has been migrated from an ESXi host to another without losing the service and in just 47 seconds, if we set up another network card this time has reduced considerably, as we have said before Vmotion is able to use multiple cards network for migration.<br>

You can consult the following white paper for reference and Best Practices see different and if you want to see new features in VMware vSphere ® vMotion ® Architecture, Performance and Best Practices in VMware vSphere ® 5.<br>








