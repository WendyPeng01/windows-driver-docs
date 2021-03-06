---
title: Properties for WIA Scanner Minidrivers
author: windows-driver-content
description: Properties for WIA Scanner Minidrivers
ms.assetid: 9de8694a-0d19-4945-b0c1-a3c4bc71dad3
---

# Properties for WIA Scanner Minidrivers


## <a href="" id="ddk-properties-for-wia-scanner-minidrivers-si"></a>


The following lists contains all of the WIA properties that are unique to WIA scanner minidrivers.

### Required Properties on Scanner Root Items (Microsoft Windows XP and Windows Me)

A WIA minidriver supplies the following properties:

[**WIA\_DPS\_OPTICAL\_XRES**](https://msdn.microsoft.com/library/windows/hardware/ff551409)

[**WIA\_DPS\_OPTICAL\_YRES**](https://msdn.microsoft.com/library/windows/hardware/ff551410)

### Optional Properties on Scanner Root Items (Windows XP and Windows Me)

A WIA minidriver supplies the following properties:

[**WIA\_DPS\_DITHER\_PATTERN\_DATA**](https://msdn.microsoft.com/library/windows/hardware/ff551376)

[**WIA\_DPS\_DITHER\_SELECT**](https://msdn.microsoft.com/library/windows/hardware/ff551377)

[**WIA\_DPS\_FILTER\_SELECT**](https://msdn.microsoft.com/library/windows/hardware/ff551392)

[**WIA\_DPS\_MAX\_SCAN\_TIME**](https://msdn.microsoft.com/library/windows/hardware/ff551403)

[**WIA\_DPS\_PAD\_COLOR**](https://msdn.microsoft.com/library/windows/hardware/ff551412)

[**WIA\_DPS\_PLATEN\_COLOR**](https://msdn.microsoft.com/library/windows/hardware/ff551420)

[**WIA\_DPS\_SHOW\_PREVIEW\_CONTROL**](https://msdn.microsoft.com/library/windows/hardware/ff551432)

### Required Properties on Scanner Child Items Able to Transfer Data

A WIA minidriver supplies the following properties:

[**WIA\_IPS\_BRIGHTNESS**](https://msdn.microsoft.com/library/windows/hardware/ff552567)

[**WIA\_IPS\_CONTRAST**](https://msdn.microsoft.com/library/windows/hardware/ff552573)

[**WIA\_IPS\_CUR\_INTENT**](https://msdn.microsoft.com/library/windows/hardware/ff552579)

[**WIA\_IPS\_PHOTOMETRIC\_INTERP**](https://msdn.microsoft.com/library/windows/hardware/ff552640)

[**WIA\_IPS\_XEXTENT**](https://msdn.microsoft.com/library/windows/hardware/ff552661)

[**WIA\_IPS\_XPOS**](https://msdn.microsoft.com/library/windows/hardware/ff552663)

[**WIA\_IPS\_XRES**](https://msdn.microsoft.com/library/windows/hardware/ff552665)

[**WIA\_IPS\_YEXTENT**](https://msdn.microsoft.com/library/windows/hardware/ff552669)

[**WIA\_IPS\_YPOS**](https://msdn.microsoft.com/library/windows/hardware/ff552671)

[**WIA\_IPS\_YRES**](https://msdn.microsoft.com/library/windows/hardware/ff552673)

### Optional Properties on Scanner Child Items Able to Transfer Data

A WIA minidriver supplies the following properties:

[**WIA\_DPS\_PAGE\_HEIGHT**](https://msdn.microsoft.com/library/windows/hardware/ff551416)

[**WIA\_DPS\_PAGE\_SIZE**](https://msdn.microsoft.com/library/windows/hardware/ff551417)

[**WIA\_DPS\_PAGE\_WIDTH**](https://msdn.microsoft.com/library/windows/hardware/ff551419)

[**WIA\_IPS\_INVERT**](https://msdn.microsoft.com/library/windows/hardware/ff552599)

[**WIA\_IPS\_MIRROR**](https://msdn.microsoft.com/library/windows/hardware/ff552616)

[**WIA\_IPS\_ORIENTATION**](https://msdn.microsoft.com/library/windows/hardware/ff552625)

[**WIA\_IPS\_ROTATION**](https://msdn.microsoft.com/library/windows/hardware/ff552648)

[**WIA\_IPS\_THRESHOLD**](https://msdn.microsoft.com/library/windows/hardware/ff552655)

[**WIA\_IPS\_WARM\_UP\_TIME**](https://msdn.microsoft.com/library/windows/hardware/ff552660)

### Required Properties on Flatbed Scanner Root Items (Windows XP and Windows Me)

A WIA minidriver supplies the following properties:

[**WIA\_DPS\_HORIZONTAL\_BED\_REGISTRATION**](https://msdn.microsoft.com/library/windows/hardware/ff551398)

[**WIA\_DPS\_HORIZONTAL\_BED\_SIZE**](https://msdn.microsoft.com/library/windows/hardware/ff551399)

[**WIA\_DPS\_PREVIEW**](https://msdn.microsoft.com/library/windows/hardware/ff551422)

[**WIA\_DPS\_VERTICAL\_BED\_REGISTRATION**](https://msdn.microsoft.com/library/windows/hardware/ff551442)

[**WIA\_DPS\_VERTICAL\_BED\_SIZE**](https://msdn.microsoft.com/library/windows/hardware/ff551445)

### Required Properties on Document Feeder Scanner Root Items (Windows XP and Windows Me)

A WIA minidriver supplies the following properties:

[**WIA\_DPS\_DOCUMENT\_HANDLING\_CAPABILITIES**](https://msdn.microsoft.com/library/windows/hardware/ff551379)

[**WIA\_DPS\_DOCUMENT\_HANDLING\_SELECT**](https://msdn.microsoft.com/library/windows/hardware/ff551384)

[**WIA\_DPS\_DOCUMENT\_HANDLING\_STATUS**](https://msdn.microsoft.com/library/windows/hardware/ff551386)

[**WIA\_DPS\_HORIZONTAL\_SHEET\_FEED\_SIZE**](https://msdn.microsoft.com/library/windows/hardware/ff551401)

[**WIA\_DPS\_MIN\_HORIZONTAL\_SHEET\_FEED\_SIZE**](https://msdn.microsoft.com/library/windows/hardware/ff551405)

[**WIA\_DPS\_MIN\_VERTICAL\_SHEET\_FEED\_SIZE**](https://msdn.microsoft.com/library/windows/hardware/ff551407)

[**WIA\_DPS\_PAGES**](https://msdn.microsoft.com/library/windows/hardware/ff551414)

[**WIA\_DPS\_SHEET\_FEEDER\_REGISTRATION**](https://msdn.microsoft.com/library/windows/hardware/ff551430)

[**WIA\_DPS\_VERTICAL\_SHEET\_FEED\_SIZE**](https://msdn.microsoft.com/library/windows/hardware/ff551446)

### Properties on Transparency Scanner Root Items (Windows XP and Windows Me)

A WIA minidriver supplies the following properties:

[**WIA\_DPS\_TRANSPARENCY**](https://msdn.microsoft.com/library/windows/hardware/ff551434)

[**WIA\_DPS\_TRANSPARENCY\_SELECT**](https://msdn.microsoft.com/library/windows/hardware/ff551437)

 

 


--------------------
[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bimage\image%5D:%20Properties%20for%20WIA%20Scanner%20Minidrivers%20%20RELEASE:%20%288/17/2016%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")


