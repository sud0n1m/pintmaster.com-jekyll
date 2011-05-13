--- 
layout: post
title: How to compile MSSQL support into PHP in Ubuntu Dapper Drake
wordpress_id: 165
wordpress_url: http://www.pintmaster.com/wordpress/index.php/20060530/how-to-compile-mssql-support-into-php-in-ubuntu-dapper-drake/
---
This information is specific to Ubuntu Dapper Drake, but it may work on other versions of the software. This will allow you to connect to Microsoft's SQL Server 2000 to use Apache and PHP to connect to a MSSQL database.
<ul>
	<li>Install support packages</li>
</ul>
<pre>sudo aptitude install freetds-dev</pre>
<pre>sudo aptitude install tdsodbc</pre>
<ul>
	<li>Modify the Freetds file to access the server: sudo nano /etc/freetds/freetds.conf <em>(not sure if this is necessary)</em></li>
</ul>
<pre># Our SQL Server
[FSData]
host = 192.168.x.x
port = 1433
tds version = 8.0</pre>
<ul>
	<li>Tell UnixODBC where to find the FreeTDS driver and give it a name:
<ul>
	<li>Modify /etc/odbcinst.ini</li>
</ul>
</li>
</ul>
<pre>[FreeTDS]
Description = FreeTDS 0.61-5 Deb
Driver = /usr/lib/odbc/libtdsodbc.so
Setup = /usr/lib/odbc/libtdsS.so
FileUsage = 1
CPTimeout = 5
CPReuse = 5</pre>
<ul>
	<li>
<ul>
	<li>Modify the odbc.ini file: sudo nano /etc/odbc.ini</li>
</ul>
</li>
</ul>
<pre>[Products]
Description = Products on Our MSSQL Server
Driver = FreeTDS
Servername = FSData
Database = Products</pre>
<ul><li>Download dpkg</li></ul>
<pre>sudo aptitude install dpkg-dev</pre> 
<ul>
	<li>Download php-src</li>
</ul>
<pre>sudo aptitude source php5</pre>
<ul>
	<li>Go into the new php5 directory</li>
	<li>Edit the debian/rules file - add the following to the common config sudo nano debian/rules</li>
</ul>
<pre>--with-mssql</pre>
<ul>
	<li>build dependencies</li>
</ul>
<pre>sudo aptitude build-dep php5</pre>
<ul>
	<li>build the package</li>
</ul>
<pre>sudo dpkg-buildpackage</pre>
<ul>
	<li>install the new PHP w/ MSSQL</li>
</ul>
<pre>sudo dpkg -i php5_5*.deb</pre>
<ul>
	<li>copy the new libphp5.so to the correct directory (otherwise it will still use the old one)</li>
</ul>
<pre>sudo cp ~/php5-*/apache2-build/libs/libphp5.so /usr/lib/apache2/modules/libphp5.so</pre>
<ul>
	<li>restart Apache</li>
</ul>
<pre>sudo /etc/init.d/apache2 restart</pre>
