--- 
layout: post
title: How to Use the Ipod (v3) with Redhat Linux 9.0
excerpt: "This document explains how to connect and use a "
wordpress_id: 14
wordpress_url: http://www.pintmaster.com/wordpress/20031015/how-to-use-the-ipod-v3-with-redhat-linux-90/
---
<img src="http://www.ipodlounge.com/assets/images/articles/history/1bigatn.jpg" alt="iPod v3 30gb" />
I am unsure whether this How To guide is backwards compatible with the previous versions of the <a href="http://www.apple.com/ipod/">Apple iPod</a>. I have a <a href="http://www.ipodlounge.com/articles_more.php?id=4280_0_8_0_C#2003">30 gb Ipod (v3)</a> and this has only been tested with that 
<!--more-->
<strong>Connecting the Ipod</strong>

The Windows formatted Ipod is essentially an external harddrive and can be connected as such. Out of the box, you can connect it using Firewire. I had many issues with the kernel crashing when using Firewire and ended up buying the USB 2.0 connection. The USB 2.0 connection did not change the process for mounting the drive 

Note: I would recommend anyone seriously considering using the Ipod on the current 2.4 kernel to buy the USB 2.0 cable. The issues with Firewire may be resolved with the 2.6 kernel 


<ol>
	<li>Make sure you are logged in as Root to install the Ipod. After the install you will not need to be root</li>
	<li>In order to find the drive try typing the command dmesg </li>
	<li>Look for a message talking about a usb / firewire harddrive on<code> /dev/</code>
</li>

	<li>To look at the structure of the hard drive, type <code>fdisk /dev/sda </code>
</li>

	<li>Create a mount point for the drive by typing <code>mkdir /mnt/Ipod</code>
</li>

	<li>Attempt to mount the drive: <code>mount -t msdos /dev/sda</code></li>


	<li>Once connected, you should be able to see the contents of the drive. Type: cd /mnt/Ipod then type ls to display the list of files. It should look something like this:
<code>[you@yourbox Ipod]# ls
bootex.log Calendars Contacts iPod_Control Movies Notes</code> </li>

	<li>
Unmount the ipod now to prepare for the next part:
<code>[you@yourbox Ipod]# cd /
[you@yourbox Ipod]# umount /mnt/Ipod </code></li>

</ol>
<strong>Making the Ipod Permanent</strong>

Once you have tested that the Ipod works and you can see some files, it is time to make it load with a simple <code>mount /mnt/Ipod </code>

<ol>
	<li>Open up <code>/etc/fstab</code> in your favorite editor. I use the command <code>emacs /etc/fstab</code></li>

	<li>
Create a line that looks like this replacing sdb2 for the location of your Ipod
<code>/dev/sdb2	/mnt/Ipod	vfat	defaults, uid=500, user, noauto	0 0</code></li>

	<li>Now we are ready to try loading the Ipod from the fstab!
<code>[you@yourbox Ipod]# mount /mnt/Ipod </code></li>


</ol>

Now you have your Ipod ready to be mounted on command!

Take a look at <a href="http://gtkpod.sourceforge.net/">GTKPOD</a>
