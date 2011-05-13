--- 
layout: post
title: Move iTunes to an external drive on your Mac - intelligently
wordpress_id: 264
wordpress_url: http://www.pintmaster.com/20061109/move-itunes-to-an-external-drive-on-your-mac-intelligently/
---
<img align="right" id="image266" src="http://www.pintmaster.com/wp-content/uploads/2006/11/external_drive.png" alt="External Drive" />There are a few ways to move your iTunes collection to a different location. Here is an intelligent way that leverages the *nix underpinnings of Mac OS X using symbolic links.

<!--adsense#TopAds-->
<ol>
	<li>Close iTunes</li>
	<li>Locate your music collection in the Finder (it should be the folder "iTunes" under "Music" in your home folder</li>
	<li>Move it to the new location! Just drag and drop, we're going to fix it in a second</li>
	<li>Right click on iTunes in the new location and select "Make Alias"</li>
	<li>Move the alias to the location your old iTunes folder is. It is probably called "iTunes alias" or similar</li>
	<li>Drag your old iTunes library to the trash</li>
	<li>Rename "iTunes Alias" to "iTunes"<a id="p265" rel="attachment" class="imagelink" href="http://www.pintmaster.com/20061109/move-itunes-to-an-external-drive-on-your-mac-intelligently/itunes-alias/" title="iTunes Alias"><img align="right" id="image265" src="http://www.pintmaster.com/wp-content/uploads/2006/11/itunes_alias.thumbnail.png" alt="iTunes Alias" /></a></li>
	<li>Open up iTunes and check to see that your music is still there and working!</li>
</ol>

This gives you flexibility if you need to reorganize or free up space. By creating an alias (symbolic link), iTunes treats the music collection as if it was never moved!
