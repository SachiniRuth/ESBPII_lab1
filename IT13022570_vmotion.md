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








