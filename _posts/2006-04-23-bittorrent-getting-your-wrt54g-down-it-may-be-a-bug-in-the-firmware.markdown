--- 
layout: post
title: Bittorrent getting your WRT54G down? It may be a bug in the firmware.
wordpress_id: 141
wordpress_url: http://www.pintmaster.com/wordpress/index.php/20060423/bittorrent-getting-your-wrt54g-down-it-may-be-a-bug-in-the-firmware/
---
I was recently playing around with ¬µTorrent and I ran across the following information on <a href="http://www.utorrent.com/faq.php#Special_note_for_users_with_Linksys_WRT54G_GL_GS_routers">problems with the WRT54G</a>. Luckily, I am using <a href="http://www.dd-wrt.com/">DD-WRT</a> on all 3 of the WRT54Gs that blanket my house. This is one of ¬µTorrent's recommended firmwares and there is a fix!

It seems that the WRT54G keeps logs of all connections for 5 Days which very quickly brings down the router when you have a ton of connections opening up through bittorrent, or any other P2P application. This little trick saved me a ton of time!
