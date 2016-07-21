---
layout: post
title:  "How-To Install Ubuntu."
excerpt: "Ubuntu is Linux based open source operating system which is basically designed for programming addicts."
date:   2016-07-20 13:25:35 +0200
categories: blog
author: shilpi_agrawal
share: true
tags: [dual-boot, ubuntu, os]
modified: 2016-07-20T16:04:57-04:00
image:
  feature: ubuntu.jpg
---
	
# UBUNTU INSTALLATION

While Ubuntu is one of the widely used Linux distros, getting your hands on it is a must-know thing for most people entering the software field.

There are a number of different ways of installing Ubuntu. In this guid I'm gonna walk you through one such way.

Ubuntu can be installed in various scenarios.

* You may install Ubuntu on a computer with no operating system at all.

* You may install Ubuntu with some other operating system.

Also installing Ubuntu with other operating system,(also termed dual-booting) there are various ways.

* Install Ubuntu from USB Stick.

* Install it using Virtual Machine.

* Install it using wubi installer i.e. especially designed for Windows 8.

In this post we will see how to install dual boot Ubuntu alongside another operating system, in our case it's Windows.

Let's begin. :D

## Download and Get Ready:

1. **Download Ubuntu:** Download your preferred version of Ubuntu such as Ubuntu 14.04, 15.10, 16.04 and there's a lot more versions, latest being 16.04. You can easily get any of its versions just by clicking here. Download time of this huge file of more than 1GB totally depends on your bandwidth speed. If your on BSNL, we're on the same boat. :P

2. **Burn your CD or create a boot able USB stick:** For this step you need software which is designed especially for Ubuntu i.e. .Universal USB Installer. There are a lot more installers to solve this purpose, this is more promising.

3. **Configure your BIOS**. Enter your systems boot settings(BIOS) and set boot order option. Entering Boot settings various between various models, so google to find the key to enter the Boot settings.So, whenever your computer starts, press the BIOS key. My case it was - F2 Key.

4. Plug in your USB stick/Live CD and restart the machine. After entering to the setup, select the device you want to boot: - live CD or USB stick. The installer will automatically take you to this screen. 

	<figure>
		<img style="margin-left: 15%;" src="/images/ubuntu_install_1.png" alt="image">
	</figure>

	Whether you want to install it or try it, you will have to follow the same procedures.

	After booting from your live CD or USB, you will get to the Try or Install window. Before you start the installation, make sure your computer is connected to the Internet. If your network connection is not working, Click Try Ubuntu and let it load. Then go to the top right 
		
		** Click on the gear icon -> select System settings -> Additional Drivers -> it will search for the drivers for the network adapter -> click on the drivers to install -> then from the Desktop select Install Ubuntu. **

5. Before beginning the installation, system will need three necessary things.
		1. Connection to the power source.
		2. Connection to the network.
		3. At least 4.8 GB free in your hard drive.

	<figure>
		<img style="margin-left: 15%;" src="/images/ubuntu_install_2.1.png" alt="image">
	</figure>

	You can proceed when you have all these set up, although the first two are not absolutely necessary.

6. For installation you will have three options in dialog box, select third option. i.e. Something else. Select it and click Install Now. We're almost Done, but coming next is the tricky part.

	<figure>
		<img style="margin-left: 15%;" src="/images/ubuntu_install_3.jpg" alt="image">
	</figure>

	While installation is going on you’ll get the information about your unallocated space and allocated space. Select one of the unallocated space in which you want to install Ubuntu.

	<figure>
		<img style="margin-left: 15%;" src="/images/ubuntu_install_2.png" alt="image">
	</figure>

See, this is where you are going to instruct the machine about the memory settings.

*We need to create three partitions.*

* Select the unallocated space or drive, click on (+) , a new dialog box will appear. In the drop down menu select swap area and the size will depend on your RAM size. i.e 1GB of Swap would be perfect for a system with 4GB RAM. Now, do the Math. :P

* Get back to the same dialog box, press Add. In the drop down menu of the new dialog box, select mount point as /boot and size will be 512 MB.

* Again return back to the same dialog box, click Add. In the drop down menu of the new dialog box select mount point as / and size will be rest of the space.

And finally click on Install, and Ubuntu will start installing on your system. The progress will be shown. 

Proceed to configue Time and Network settings. 

And yes! We installed Ubuntu. Now start playing with it. Have Fun!



