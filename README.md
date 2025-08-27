i was developing a Head unit for a nav system and i realized that there are no way to use a2dp easely on a 32bit windows 10 OS so i added support for CLI to this software

# AudioPlaybackConnector
**English** 

Bluetooth audio playback (A2DP Sink) connector for Windows 10 2004+.

Microsoft added Bluetooth A2DP Sink to Windows 10 2004. However, a third-party app is required to manage connection.\
There is already an app can do this job. However it can't hide to notification area and it's not open-source.\
So I write this app, provide a simple, modern and open-source alternative.

# Preview
![Preview](https://cdn.jsdelivr.net/gh/ysc3839/AudioPlaybackConnector@master/AudioPlaybackConnector.gif)

# Usage
* Download and run AudioPlaybackConnector from 
* Add a bluetooth device in system bluetooth settings. You can right click AudioPlaybackConnector icon in notification area and select "Bluetooth Settings".
* Click AudioPlaybackConnector icon and select the device you want to connect.
* Enjoy!
# CLI usage:
exucutable.exe dispositivi connetti "bluetooth id" -allows you to connect to the bluetooth device you putted the id off in the ""
executable.exe dispositivi -will return a list of compatible devices
the app doesn't allow you to add devices to your bluetooth paired devices, i resolved this issues by obligating windows to always be visible with this reg key:
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Bthport\Parameters" /v DiscoverableMode /t REG_DWORD /d 2 /f
