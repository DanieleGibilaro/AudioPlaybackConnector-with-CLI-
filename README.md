# why this exist?
while developing a Nav Head unit on a obligated win32 based machine i've realized that there are no easy way to use bluetooth a2dp on a 32bit windows 10 by python or other scripting/programing languages, so ive modified this app to allow you to comunicate with it by CLI
# AudioPlaybackConnector
**English** |

Bluetooth audio playback (A2DP Sink) connector for Windows 10 2004+.

Microsoft added Bluetooth A2DP Sink to Windows 10 2004. However, a third-party app is required to manage connection.\
There is already an app can do this job. However it can't hide to notification area and it's not open-source.\
So I write this app, provide a simple, modern and open-source alternative.

# Usage
* Download and run AudioPlaybackConnector from RElease
* Add a bluetooth device in system bluetooth settings. You can right click AudioPlaybackConnector icon in notification area and select "Bluetooth Settings".
* Click AudioPlaybackConnector icon and select the device you want to connect.
* Enjoy!

# how to use CLI and some tips
* executable.exe dispositivi -show you a list of devices that are already paired and can be used for a2dp audio
<br>\
The output will be something like: devicename@id
<br>\
 executable dispositivi connetti "id" -will start the app and automaticaly connect to the device id you have specified
<br>\
to disconnect just simply explode(close it, but saying explode is much better) the process
<br>\
for my specific scenario i had to be able to pair devices easily so i add this reg key to obligate windows to be always visible :
<br>\
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Bthport\Parameters" /v DiscoverableMode /t REG_DWORD /d 2 /f
