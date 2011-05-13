--- 
layout: post
title: How to find out who is sending you spam using email headers and visual route
excerpt: VisualRoute Server, pings / whois / traceroutes.  This How-to shows you how to use this to find out where your spam is coming from.
wordpress_id: 31
wordpress_url: http://www.pintmaster.com/wordpress/20041124/nedcomp-hosting-visualroute-server-pings-whois-traceroutes/
---
A lot of spam these days has spoofed headers. Some of the spam I receive says it is coming from me to me, or even from the people I do business with. We can examine the email header to determine who actually sent the email. 

<ol>
	<li>Open your email client and find a spam message - shouldnt be hard these days. The one I will be using claims to be from Suntrust Bank and looks like this:<br><img src="http://www.pintmaster.com/wordpress/wp-content/suntrust.png" alt="Suntrust Phishing Scam" /> </li>
	<li>I use Outlook 2003 at work so as you can guess, finding the headers is a little less intuitive than other email clients. First, double click on the email to open it in a separate window. Then, click "View -> Options". You should have an email header that looks something like this:
<code>
Microsoft Mail Internet Headers Version 2.0
Priority: normal
Importance: normal
thread-index: AcTFH98jKHBYsxN5RGKIBDEI/WSbTA==
X-iHateSpam-Quarantined: Quarantined by iHateSpam Server Edition (389)
Content-Transfer-Encoding: 7bit
Content-Class: urn:content-classes:message
Received: from my1.email.net ([11.111.111.111]) by my2.email.net with Microsoft SMTPSVC(6.0.3790.211); Sun, 7 Nov 2004 18:16:26 -0500
Received: from <strong>80.117.48.160 ([80.117.48.160])</strong> by my1.email.net with Microsoft SMTPSVC(5.0.2195.6713); Sun, 7 Nov 2004 18:16:23 -0500
From: "SunTrust bank" < -support56@suntrust.com>
To: <netco @netcousa.com>
Subject: SunTrust Bank Online
Date: Mon, 8 Nov 2004 12:16:19 +0100
MIME-Version: 1.0
Content-Type: multipart/related;
	type="multipart/alternative";
	boundary="----p5940362j9160295h3829588q7938T27"
X-Mailer: AOL 7.0 for Windows US sub 118
X-MimeOLE: Produced By Microsoft MimeOLE V6.00.3790.181
Return-Path: <w4e95015 @earthlink.net>
Message-ID: (ex2ger4uis42nxhwgrr000011c4 @ex2.callihq.net )
X-OriginalArrivalTime: 07 Nov 2004 23:16:24.0157 (UTC) FILETIME=[CCAA08D0:01C4C51F]
... More stuff down here...</w4e95015></netco></></code>
</li>
	<li>What we are looking for is the IP address of the spammer or the spam relay that sent the email to us. We can see that it is <code>80.117.48.160</code> because this is the address that doesnt belong to our email server and it is also the original server that our server received the email from.</li>
	<li>Now for the fun part! (2004/11/29 EDIT - Visualroute server is no longer there, possible to use ip2location.com)Lets put their IP address into the <a href="http://www.ip2location.com/free.asp">IP2Location</a> to see where they hang out. <br><img src="http://www.pintmaster.com/wordpress/wp-content/visualroute.png" alt="VisualRoute Image" />
It looks like this email most likely came from Milan, Italy.  So now you have a way to track down who is sending you emails by their geographical location
 
</li></ol>
How to use this information<ul>
	<li><a href="http://www.senderbase.org/search?searchString=interbusiness.it">Check interbusiness.it in Senderbase</a> - a website to check out how much email they send - From there you can find the abuse email address and send them an copy of the <strong>email header</strong> you received. It is important to send the header because they will not be able to track down the spammers without their IP address that is in the header. If they are decent, they will deal with the spammers, if not your time has been wasted.</li>

</ul>
