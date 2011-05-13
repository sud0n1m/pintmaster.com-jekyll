--- 
layout: post
title: installing google desktop under different credentials than the active user is currently not supported
wordpress_id: 294
wordpress_url: http://www.pintmaster.com/20061215/installing-google-desktop-under-different-credentials-than-the-active-user-is-currently-not-supported/
---
I was recently trying to uninstall Google Desktop from my Windows XP install that I had running in Parallels Desktop for Mac. Every time I would boot up, it would tell me that it could not upgrade the database and begin reindexing all my emails and files from 0%. Thats no good! So, I decided to uninstall it and give Windows Desktop Search 3.0 a try.

Well, when I tried to uninstall google desktop, I would get the error message: "installing google desktop under different credentials than the active user is currently not supported". After some research, and frustration, I found someones recommendation. If  you get this error, the steps are as follows.

<ol>
	<li>Run the google desktop uninstall</li>
	<li>Click OK on the first error message, but leave the second one up</li>
	<li>Start the google desktop uninstaller again</li>
	<li>Click yes to all of the questions!</li>
	<li>Restart.</li>
</ol>

That should enable you to remove Google Desktop, when Google Desktop doesnt want to be removed!
