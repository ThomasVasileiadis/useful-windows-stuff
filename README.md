**Network Troubleshooting**
---------------------------------------------------------------------

**Reset TCP/IP commands:**
* netsh winsock reset

* netsh int ip reset

  
**Reset the IP and obtain a new one:**
* ipconfig /release

* ipconfig /renew

* ipconfig /flushdns

**Make internet conenction stable**
* netsh interface tcp show global

* netsh int tcp set global autotuninglevel=disabled

* netsh int tcp set global autotuninglevel=normal

  
**Disabling WAN drivers for good**
* Press WindowsKey and then type services, hit enter. 

* Find a service called <b>Remote Access Auto Connection Manager</b>, right click properties, then stop the service and then switch from automatic to disabled.
  
* Find a service called <b>Secure Socket Tuneling Protocol Service</b>, and again right click properties, then stop the service and switch from automatic to disabled.
  
  Go to <b>Device Manager</b>, on <b>Network Adapters</b> right click and hit <b>Scan for changes</b>.
  Reboot and voila.
 
 
**Repairing Windows**
---------------------------------------------------------------

* sfc /scannow : (*Checks system files for possible damage and repairs it.*)

* scanreg /fix : (*Checks registry files for possible damage and repairs it.*)


**Reformating Windows partition to NTFS via cmd**
--------------------------------------------------------------------
* Shift + F10 (to open cmd)
* DISKPART
* LIST DISK
* SELECT DISK #
* CLEAN
* CONVERT MBR
* CREATE PARTITION PRIMARY SIZE=50000 (The size is in MB, so enter the amount that you want to use for your system partition)
* FORMAT FS NTFS LABEL "SYSTEM" QUICK

**Useful wordpress stuff**
--------------------------------------------------------------------
* Update the htaccess file in Wordpress
* First install YOAST SEO
* Go to tools and select edit
* paste this 
* php_value upload_max_filesize 128M
php_value post_max_size 128M
php_value memory_limit 256M
php_value max_execution_time 300
php_value max_input_time 300
