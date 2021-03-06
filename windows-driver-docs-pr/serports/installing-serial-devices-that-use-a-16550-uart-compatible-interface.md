---
title: Installing Serial Devices that Use a 16550 UART-Compatible Interface
author: windows-driver-content
description: Installing Serial Devices that Use a 16550 UART-Compatible Interface
ms.assetid: d80db651-b890-44dc-98ad-32e72e244d8c
keywords: ["Serial driver WDK , 16550 UART-compatible interfaces", "universal asynchronous receiver-transmitters WDK serial devices", "UART WDK serial devices", "16550 UART-compatible interfaces WDK serial devices"]
---

# Installing Serial Devices that Use a 16550 UART-Compatible Interface


## <a href="" id="ddk-installing-serial-devices-that-use-a-16550-uart-compatible-interfa"></a>


To install a Plug and Play device that uses Serial as a lower-level device filter driver, do the following:

-   Specify Serial as a lower-level device filter driver in the device's INF file -- see [Installing a Filter Driver](https://msdn.microsoft.com/library/windows/hardware/ff547595).

-   Set the **SerialSkipExternalNaming** entry value for the device to a nonzero value -- see [Registry Settings for a Plug and Play Serial Device](registry-settings-for-a-plug-and-play-serial-device.md).

 

 


--------------------
[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bserports\serports%5D:%20Installing%20Serial%20Devices%20that%20Use%20a%2016550%20UART-Compatible%20Interface%20%20RELEASE:%20%288/4/2016%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")


