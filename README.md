Network Troubleshooting
----------------------------------------------------------------------------------------------------------------------------------------


<b>Reset TCP/IP commands:</b>

netsh winsock reset

netsh int ip reset

  
<b>Reset the IP and obtain a new one:</b>

ipconfig /release

ipconfig /renew

ipconfig /flushdns

  
Disabling WAN drivers for good
  ----------------------------------------------------------------------------------------------------------------------------------------
  
Press WindowsKey and then type services, hit enter. 

  Find a service called <b>Remote Access Auto Connection Manager</b>, right click properties, then stop the service and then switch from automatic to disabled.
  
  Find a service called <b>Secure Socket Tuneling Protocol Service</b>, and again right click properties, then stop the service and switch from automatic to disabled.
  
  Go to <b>Device Manager</b>, on <b>Network Adapters</b> right click and hit <b>Scan for changes</b>.
  Reboot and voila.
 
 
<b> Repairing Windows </b>
----------------------------------------------------------------------------------------------------------------------------------------


sfc /scannow : Checks system files for possible damage and repairs it.

scanreg /fix : Checks registry files for possible damage and repairs it.

----------------------------------------------------------------------------------------------------------------------------------------
