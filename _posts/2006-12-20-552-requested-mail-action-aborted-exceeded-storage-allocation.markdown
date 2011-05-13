--- 
layout: post
title: "552 Requested mail action aborted: exceeded storage allocation"
wordpress_id: 302
wordpress_url: http://www.pintmaster.com/20061220/552-requested-mail-action-aborted-exceeded-storage-allocation/
---
Here's the latest ridiculous Microsoft bug I've encountered. The way to replicate is as follows.

<ol>
	<li>Reply to a message from someone in Japan (or other N. Asian countries) that uses Exchange Server 2003</li>
	<li>Format your document with a lot of tables and other things</li>
	<li>Send</li>
</ol>

For some reason, exchange 2003 panicks when you add tables into an email originally from someone in Japan, Korea or others. The explanation from microsoft is as follows:

<blockquote>The default MIME encoding in Exchange 2003 is 7-bit transfer encoding. The MIME encoding in some Asian languages must be set to an encoding method that is different from 7-bit encoding to wrap lines of text that contain more than 998 characters.</blockquote>

<a href="http://support.microsoft.com/Default.aspx?kbid=885419">See the original KB article for more</a>
