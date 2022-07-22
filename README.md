# rdp-configuration

### Fix the RDP Session Keeps Disconnecting
https://www.anyviewer.com/how-to/rdp-session-keeps-disconnecting-2578.html

### How To Optimize Your Network Adapter Settings For Higher Speeds & Lower Network Latency!
https://www.youtube.com/watch?v=aNtqzfHBKys

## Check the Local Group Policy

According to some users, this problem may also be caused by the session time limit setting. Users can change the settings to configure a time limit for disconnected Remote Desktop Services sessions.

Step 1. Press Win + R to invoke the Run dialog box. Type in “gpedit.msc” and hit OK to open Registry Editor.

Step 2. Navigate here: Computer Configuration > Administrative Templates > Windows Components > Remote Desktop Services > Remote Desktop Session Host > Session Time Limits. Find “Set time limit for disconnected session” and “Sets a time limit for active but idle Terminal Services sessions” on the right pane.

Step 3. Enable “Set time limit for disconnected session” to Never, and then enable “Sets a time limit for active but idle Terminal Services sessions” to Never.

## Change the device settings used for remote session

It has been tested by some users that unselect the option Smart cards or Windows Hello for Business helps troubleshoot the disconnection problem. Follows the steps below to make your RDP maintains connected.

Step 1. Search for Remote Desktop Connection in the search box and then start RDP. Select More Options.

Step 2. Switch to Local Resources and then click More.

Step 3. Find the option Smart cards or Windows Hello for Business and then unselect it.

## Verify Remote Desktop Services Limit number of connections policy

Sometimes, when the number of Remote Desktop Services sessions that can be active on a server is exceeded, users may keep getting disconnected. Therefore, users can follow the steps below to verify and change the number of connections that they want to allow.

Step 1. Press Win + R to invoke the Run dialog box. Type in “gpedit.msc” and hit OK to open Registry Editor.

Step 2. Navigate here: Local Computer Policy > Computer Configuration > Administrative Templates > Windows Components > Remote Desktop Services > Remote Desktop Session Host > Connections. Find Limit number of connections.

Step 3. Click Enabled. In the RD Maximum Connections allowed box, type the maximum number of connections that you want to allow, and then click OK.

## Disable restriction on Remote Desktop session

You can also change the Group Policy setting to allow users to make unlimited simultaneous remote connections by using Remote Desktop Services. This may also help solve the disconnection problem caused by the number of Remote Desktop sessions.

Step 1. Navigate here: Computer Configuration > Administrative Templates > Windows Components > Remote Desktop Services > Remote Desktop Session Host > Connections. On the right pane, find Restrict Remote Desktop Services users to a single Remote Desktop Services session and double-click it.  

Step 2. Then disable the policy setting.
