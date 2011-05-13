--- 
layout: post
title: Mac OS X and Xen Optimizer? Is this relationship the future of Windows on the Mac?
wordpress_id: 119
wordpress_url: http://www.pintmaster.com/wordpress/20060131/mac-os-x-and-xen-optimizer-is-this-relationship-the-future-of-windows-on-the-mac/
---
I had a really interesting conversation with a <strike>guy from</strike> founder of <a href="http://xensource.com/">XenSource</a>, Moshe Bar last weekend. He sent me an instant message and since these guys <strike>will</strike> may at some point be able to provide an alternative to dual booting the Intel Mac, I was interested to learn some more.

What I found out from him was pretty interesting stuff. For those of you that are unfamiliar with Xen and what it does, I will try to explain in a very high level way (which is the extent of my understanding). Xen loads right after the computer boots up, and loads into memory. Xen sits as an interface between the operating system and the hardware. This gives Xen the ability to allocate resources when running multiple operating systems; i.e. virtualization. You are able to run more than one OS, not running one on top of another, but side by side, simultaneously.

I bet some of  you are thinking: What is the cost to my resources to run Xen?  Xen costs you approximately 1% of your system resources to run it. Not too bad.

At the moment, the Xen guy told me that using Xen, he is able to run <strike>Windows XP</strike> <em>Linux</em> and Freebsd on the Intel Mac, (his iMac) but not Mac OS X. What???  Well, that's what he said. I would really like to see that. The time frame for Mac OS X running on Xen is likely 4Q '06. This, however, is his pet project and not an official XenSource project.
The other interesting thing we talked about is how Mac OS X currently interfaces with the hardware. I am really unfamiliar with much more than the buzzwords, so I will do my best to explain. Currently, Apple uses the <a href="http://en.wikipedia.org/wiki/Mach_kernel">Mach Kernel</a> to interface with the hardware. However, "Mach" is essentially outdated and causes a lot of the bottlenecks with programs having to create a lot more processes than necessary to get the job done. The guy from Xen told me they have been talking a great deal with the Apple guys about replacing Mach with Xen. This is a really big deal! This would be consistent with reports that Apple has <a href="http://www.macsimumnews.com/index.php/archive/apple_files_patent_system_and_method_for_creating_tamper_resistant_code/">filed patents related to Virtualization</a>.

The reason Apple has not switched OS X to use Xen instead of Mach yet according to the <strike>guy at Xen</strike> Moshe is because XenSource has not yet implemented the system to support the intensive graphics requirements of Mac OS X.

My prediction is that in OS X 10.6, we will see some sort of fast-user switching between operating systems. Is that realistic, or am I just dreaming?

EDIT: I have corrected this - apparrently he has not been able to run Windows yet since he says this requires Intel's VT CPUs.

Update: I referred a reporter from <em>Computer World</em> to Moshe Bar, the guy with whom I spoke. In <a title="Computer World Article" href="http://www.computerworld.com/softwaretopics/software/story/0,10801,108532p4,00.html">this article</a>, Moshe clarifies some of the things I was confused on. I got a few very key details wrong.

..
