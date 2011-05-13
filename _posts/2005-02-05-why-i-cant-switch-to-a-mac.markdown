--- 
layout: post
title: Why I cant switch to a Mac for work
wordpress_id: 45
wordpress_url: http://www.pintmaster.com/wordpress/20050205/why-i-cant-switch-to-a-mac/
---
Just over a year ago, I purchased a beautiful new Powerbook G4 1.25 Ghz computer from my campus computer store. After starting work, my great computer was collecting dust and I was frustrated. So, I asked my boss if I could use it as a replacement for my work computer. He agreed. We have an all-Microsoft office. When I say all, I mean ALL. We run Exchange 2003 and Windows file sharing with large repository for our shared files. Most people in the office have IBM laptops running Windows XP to connect in. I use an IBM desktop. All our computers are under 2 years old.

<strong>Email</strong>
The first task and unfortunately the ultimate deciding factor was Email support. In my business we send a lot of documents to people so Microsoft Office is a must whether you are on Mac or PC. So, I fired up Microsoft Entourage 2004, the Mac equivalent of Outlook. I put in my account information and hit ok. The first thing I noticed, is that Entourage tells you that it uses Outlook Web Access, and not the regular exchange protocol. My question to Microsoft is: Why would you do this!?!??!?. The impact of this decision is well documented online in the message boards. It makes your outlook access very SLLOOOOOOWWWW. How slow is it? If Entourage is not in the foreground, it wont download new messages. When entourage is in the foreground, it can take up to 5 minutes to start downloading new mail. It seems to go through every folder and subfolder I have synchronizing even when there are no changes. It gives no precedence to the inbox which, in my first day of work probably took me 40 minutes to see a new message after it had arrived. As a speed comparison, it ended up being faster for me to run Outlook 2003 in a Windows XP virtual PC. 

<em>Calendar, Tasks and Address Book</em>
This was not the only issue. The calendars synchronize but not perfectly. It seems as though they overlap days. Tasks DO NOT synchronize and there is no way to make this work. Contacts are also less than perfect. In our setup, we have a large repository of contacts in a public folder. I am able to make this my default address book when composing email. I cant even see this address book in Entourage.

<em>Composing Email</em>
Outlook offers an option to use Word to compose email. I started using this option to make our correspondence look more professional. One feature which is extremely useful is the ability to put in an HTML table. Entourage allows composition in HTMl, but not inserting tables. What the heck were they thinking? Well, after some research, I stumbled upon other Entourage users asking about this. The solution is, compose it in Word and then click send as HTML email from the file menu. Well, this solution is not that great. It is a pain! Not only this, I saved one of my templates from Outlook as a word document opened it in Word on the Mac. It looked fine. Then I made my changes and clicked send as HTML email, and it made everything look green. I was unable to find a good solution to this except for redoing the entire document which seemed to work, however, there were some other irregularities when viewing the sent message. This was a huge annoyance and a big deal. 
<strong>
Word, Excel, Powerpoint</strong>
All of these programs worked acceptably. I have no major problems, and output on my Mac looked the same on other people's PCs. The one big annoyange is with powerpoint. Microsoft decided not to implement the Windows version of Powerpoint's default view with the small preview of the slides. This is a pretty useful view of your slides and is implemented in Apple's Keynote, which in my opinion is a better presentation tool than powerpoint on both windows and the Mac.

<strong>Windows File Sharing</strong>
Samba on the mac has gotten much better, but it still does not do several important things as easily as windows.
<ol>
	<li>Automounting - I understand that this can probably be done using some sort of startup script, but with a laptop, I didnt want to deal with tons of error messages </li>
	<li>Synchronizing - I use a free tool to backup my documents to the network drive at the end of the day. I didnt find an easy replacement in my short time with my Mac</li>
	<li>Finding computers - This has never worked well. OS X does not adequately find all the computers on the network</li>
</ol>

<strong>Database</strong>
I recently set up a database for tracking some information in the company. I used Microsoft Access 2003. There is no Microsoft equivalent to Access on OS X. I evaluated using Filemaker to do this and wanted to use it as a frontend for MySQL. This didnt go well in two areas. Since I hadnt already set up my database in Filemaker, I would have to find some way to get my access database ported to Filemaker. There was no tool built into filemaker to convert the access database. Then, I would have to try and figure out how to connect filemaker to MySQL. I understand that this can be done using MyODBC and had this tool set up to log on to the MySQL database. However, I was never able to get Filemaker to recognize the MyODBC connection. So, I decided to just do my database work on my old computer. With access I had the benefit of easy import and export with Excel as well as Pivot tables built in - quite possibly the most useful feature in the office suite.

<strong>Conclusions</strong>
After my trials and tribulations, I came to the following conclusions:

Entourage is not ready for use in an Exchange 2003 environment.
Composing email on the Mac is not as sophisticated yet as it is in Windows
Word, Excel and Powerpoint interoperate acceptably
Operating on a Mac in an all-Windows office takes more time than it is worth.

As many flaws as Windows has, it has a death grip on the businesses of the world. In my business, it is almost guaranteed that everyone uses the Microsoft suite of business products. It makes it easier when you have to talk to each other. The way microsoft works, there is an almost certainty that a document created in a Microsoft product will not work the same in a non-microsoft product. This works the other way too and was most frustrating in trying to get my email working. After four days of trying to make it work, I found myself less productive because I couldnt do things the way I had been. I ended up booting into my virtual pc and using remote desktop to use my old computer (the native remote desktop is too slow). The lacking features made me slower and less productive. 

I still look forward to a time when I can use my Mac at work. I think if we werent running Exchange 2003 and used IMAP and an LDAP directory it would be. Maybe the next version of Entourage will work. I sure hope so.
