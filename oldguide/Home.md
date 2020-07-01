**Welcome to the PSNaviGuide!**

> Disclaimer:  
> This guide isn't being actively maintained anymore as I haven't got Driver4VR installed anymore because I'm going to get a Rift S soon.  
> A list with currently confirmed setups will be on the [last page of the setup](https://github.com/m004/PSNaviGuide/wiki/Input-mapping-and-offseting) at troubleshooting.  
> No liability if this procedure isn't working.

This guide should help you set up your PSNavi controllers in combination with your moves.
If you have gathered all parts, this should only take 10-30 minutes.

# Preparing
This guide requires you to have a fully set up Driver4VR setup with PSMoveService. If you haven't done it yet, I'm recommending following guides for you:
* [https://www.youtube.com/watch?v=lJyIHCMDINA by Lordmodder85](https://www.youtube.com/watch?v=lJyIHCMDINA)
* [https://www.youtube.com/watch?v=wONnC5GJigo by Lordmodder85](https://www.youtube.com/watch?v=wONnC5GJigo)

The PSMoveService wiki is also a good source of information: <https://github.com/psmoveservice/PSMoveService/wiki>

If you have a complete setup, gather the following hardware parts:
* 1-2 PSNavi
* One joiner clip for each PSNavi  
As the Navi doesn't have any sensors and tracking LEDs, you need to connect them with a PSMove to use the sensors and tracking from the move.  
If you have a 3D printer or want to use a service like Shapeways or Craftcloud, there is a 3d model from Xierion on the initial PSNavi guide by PSMoveService: [PSNavi-Setup](https://github.com/psmoveservice/PSMoveService/wiki/PSNavi-Setup)  
There is a DIY solution too from Daley Tech utilizing Silicone and Corn Starch: <https://www.youtube.com/watch?v=z8cKPm8ByJU>
* 1 Mini USB cable  
Required for pairing the PSNavi controllers with the software.

Now if you have all parts, download the following software:
* [The latest release of BthPS3 by nefarius](https://github.com/ViGEm/BthPS3/releases)  
In earlier days you needed two bluetooth dongles and SCPTool because the PSNavi hasn't got a proper HID interface. With this driver, it is possible to only need one bluetooth dongle.
* [The latest release of devreorder by briankendall](https://github.com/briankendall/devreorder/releases)  
You need this piece of software because D4VR has some issue with the several Motion Controller devices filling up the device list. In my case, the solution using devreorder worked fine.

**tl;dr:**
### Essential
* Fully complete Driver4VR setup with PSMoveService
### Hardware Requirements
* 1-2 PSNavi
* One joiner clip for each PSNavi
* Mini USB cables depending on how many Navis you have
### Software Requirements
* [The latest release of BthPS3 by nefarius](https://github.com/ViGEm/BthPS3/releases)
* [The latest release of devreorder by briankendall](https://github.com/briankendall/devreorder/releases)

Next page: [Initial Setup](https://github.com/m004/PSNaviGuide/wiki/Initial-Setup)
