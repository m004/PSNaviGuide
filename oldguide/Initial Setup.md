Install the BthPS3 driver and go to "Show Next Steps". Follow each of the Post-Setup instructions.  
After this, you should have Shibari ready to use. Put it in a safe place where you can access it easily because you'll need that program to use the PSNavis.  
Start it up and connect the PSNavi controllers with Mini-USB to pair them.  
Disconnect them now and make sure the Navi is either having it's LED on permanently or make sure the Navi's led is blinking.  

Now, unzip the devreorder file at a temporary directory.  
Before you continue, make sure to disconnect every controller (+ Steering Wheels, etc.) except the PSNavi controllers. You don't need to disconnect the PSMoves.  
First, download my prepared [devreorder.ini](https://github.com/m004/PSNaviGuide/raw/master/files/devreorder.ini) file and replace it in the temporary directory (Right-Click link and go to save).  
Go to the temporary directory, open DeviceLister.exe and open the prepared devreorder.ini with an editor like Notepad++. 
 
Look at the DeviceLister.exe you've opened, there should be some devices in the application.  
Copy the GUID from the entry with the name "Controller (XBOX 360 For Windows)" so you have something like this in your clipboard:
`{6a6535e0-cd6c-11e8-8001-444553540000}`  
Then replace the ReplaceMe in the devreorder.ini with the GUID you copied.  
If you want to setup two PSNavis, copy the GUID from the other "Controller (XBOX 360 For Windows)" entry and replace the ;ReplaceMe2 in the devreorder.ini.
devreorder.ini should look like this:
```
; devreorder settings for PSNavi-Usage
; Replace the ReplaceMe tags with the GUID from the Virtual Xbox 360 Controller
; Example for GUID: {6a6535e0-cd6c-11e8-8001-444553540000}

[order]

{6a6535e0-cd6c-11e8-8001-444553540000}
{12345abc-def6-ghij-1234-123456789012}
Motion Controller

[hidden]

Motion Controller

[visible]


[ignored processes]


```

Copy the devreorder.ini and the dinput8.dll from the x64 folder in the temporary folder to the Driver4VR folder (Example: "C:\Program Files (x86)\Driver4VR")

To finish the initial setup, %appdata%\PSMoveService and backup the DeviceManagerConfig.json. Then, edit the original DeviceManagerConfig.json and verify that the gamepad_api_enabled is false. If not, change it so it looks like this:  
```
    "gamepad_api_enabled": "false",
```  
The entire DeviceManagerConfig.json should now look like this (Don't mind the other values for this, the gamepad_api_enabled is important):

```
{
    "version": "1",
    "controller_reconnect_interval": "0",
    "controller_poll_interval": "2",
    "tracker_reconnect_interval": "10000",
    "tracker_poll_interval": "13",
    "hmd_reconnect_interval": "10000",
    "hmd_poll_interval": "13",
    "gamepad_api_enabled": "false",
    "platform_api_enabled": "true"
}
```

**tl;dr**:
* Install BthPS3 and do Post-Setup
* Start Shibari, pair controllers and disconnect them, for having them on bluetooth
* Unzip devreorder zip to a temporary directory
* Disconnect every controller except the PSNavis and PSMoves
* Replace devreorder.ini with edited ini from me
* Open DeviceLister, copy the GUIDs from the "Controller (XBOX 360 For Windows)" entries and replace each ReplaceMe with the GUID
* Copy devreorder.ini and the dinput8.dll from the x64 folder to the Driver4VR folder.
* Set gamepad_api_enabled to false in %appdata%\PSMoveService\DeviceManagerConfig.json

Next page: [Input mapping and offsetting](https://github.com/m004/PSNaviGuide/blob/master/oldguide/Input%20mapping%20and%20offsetting.md)
