Open Driver4VR and etc. as you would normally. (You need to go on "Start Driver4VR" to configure the VRGamepads)
In Driver4VR go to Tracker Manager and activate VR Gamepad under the device support window.  
Then, go to Update List of Devices and you should see some VRGamepads. Go on preview to identify each PSNavi.  
Now, select a tracker and the respective VRGamepad and go to "Assign VR Gamepad". This should open a menu where you can map buttons. Map the buttons as you like, but I'm recommending that you bind the joystick as the touchpad. (If you have two controllers, do this twice)  
The last thing you need to do is offsetting the controllers in D4VR. To do so, go to Controller Shift / Offset, go the Tracker where your Navi is (or all controllers if you have 2) and change the Y value until all controllers look in VR where your hand is. 16 worked in my case.  

**tl;dr:**
* Activate VRGamepad Support under D4VR>>Tracker Manager>>Device Support
* Update Devices and identify the Navis by going on preview
* Select tracker and corresponding VRGamepad and go to assign gamepad
* Map buttons
* Offset the Y value on the controllers under Controller Shift / Offset
# Notes, Credits
Your PSNavi controllers are now fully set up and ready for usage in VR. You can now delete the temporary folder. (Do NOT delete Shibari!)  
Take care of the following things:
* I'm recommending to connect the moves before starting Shibari
* Start Shibari before Driver4VR  

If there are any issues or problems you have while doing all this, please open an issue with the problem you have and I try my best to help you.  

## Troubleshooting
* PSMove controllers are not connecting  
Try pressing the PS button right after the blinking stops. It should connect then just like normal.
* Navi is not being detected by D4VR  
If you are having an automated script make sure the working dir is the Driver4VR directory.
Example for my AHK script addressing this:  
```
SetTitleMatchMode, 2


run, "C:\Program Files\PSMoveService\bin\psmoveserviceadmin.exe"
Sleep, 1000

run, "M:\Projects\PSMove\Freepie\PSMoveFreepieBridge.exe"
sleep, 300
send, 1 {Enter}
send, 0 {Enter}
sleep, 600

run, "C:\Program Files (x86)\FreePIE\FreePIE.exe"
WinActivate, - freepie, 
Sleep, 1100

send, !f                     
send, ^o
Send, "altd4vr"{enter}
sleep, 1100
send, {f5}
sleep, 600

SetWorkingDir, C:\Program Files (x86)\Riftcat 2
run, "C:\Program Files (x86)\Riftcat 2\RiftCat.exe"

Sleep, 10000

SetWorkingDir, C:\Program Files (x86)\Driver4VR
run, "C:\Program Files (x86)\Driver4VR\Driver4VR.exe"

send, {LWin down}d{LWin up}

```

* I haven't got a Navi controller, will this guide work with a different Bluetooth compatible controller?  
This setup is probably working with any Bluetooth controller that supports DirectInput or XInput. You just don't need to install BthPS3 and you need to know your devices name under Windows. In DeviceLister look for that device name of your controller and use that GUID.

* PS Button of Navi not working  
Disable everything that interacts with the Xbox Guide Button (Example: Steam Big Picture, Game DVR)

* Confirmed setups:  
    * Windows 10 1903, Driver4VR 5.2.8.2, PSMoveService v0.9-alpha 9.0.1, BthPS3 1.2.4, CSR4.0 Bluetooth adapter, 4 PSeye cameras, 2 PS3 moves, 1 PSNavi
    * Windows 10 2004, Driver4VR 5.2.10.2, PSMoveService v0.9-alpha 9.0.1, BthPS3 1.2.4, CSR4.0 Bluetooth adapter, 4 PSeye cameras, 2 PS3 moves, 1 PSNavi
If you have a working setup using this guide, feel free to send me your configuration so I can update this list.
## Uninstalling
Go to the control panel and uninstall the following things: "BthPS3 Bluetooth Drivers", "Windows Driver Package - Nefarius Software Solutions e.U." and "ViGEm Bus Driver"  
Now, simply delete Shibari and delete the devreorder.ini and dinput8.dll in the Driver4VR folder.

## Credits
The PSMoveService Team for making [PSMoveService](https://github.com/psmoveservice/PSMoveService)  
Greg Driver for making [Driver4VR](https://www.driver4vr.com/)  
nefarius for making [BthPS3](https://github.com/ViGEm/BthPS3), [FireShock](https://github.com/ViGEm/FireShock), [Shibari](https://github.com/ViGEm/Shibari) and the [ViGEm Bus Driver](https://github.com/ViGEm/ViGEmBus)  
briankendall for making [devreorder](https://github.com/briankendall/devreorder)
