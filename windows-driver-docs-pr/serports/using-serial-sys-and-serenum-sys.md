---
title: Using Serial.sys and Serenum.sys
author: windows-driver-content
description: Using Serial.sys and Serenum.sys
ms.assetid: 2dcf22c8-0666-4b58-8fd3-97a4d17eaa2a
keywords: ["serial ports WDK", "serial devices WDK", "ports WDK , serial", "universal asynchronous receiver-transmitters WDK serial devices", "UART WDK serial devices", "function drivers WDK serial ports", "serial drivers WDK", "16550 UART-compatible interfaces WDK serial devices", "lower-level device filter drivers WDK serial devices", "higher-level device filter drivers WDK serial devices", "filter drivers WDK serial devices"]
---

# Using Serial.sys and Serenum.sys


## <a href="" id="ddk-serial-devices-and-drivers-kg"></a>


Starting with Windows 2000, the following system components are available for use with serial controller devices that have hardware interfaces that are compatible with the 16550 universal asynchronous receiver-transmitter (UART):

-   Serial and Serenum drivers

    Serial.sys (Serial) is a system-supplied function driver for serial devices. You can also use Serial as a lower-level device filter driver for any type of Plug and Play device that requires a 16550 UART-compatible interface.

    Serenum.sys (Serenum) is a system-supplied upper-level device filter driver that you can use in conjunction with Serial (or a vendor-supplied function driver) to provide the function of a Plug and Play bus driver for an RS-232 port.

    For more information about the operation of Serial and Serenum, see the following topics:

    -   [Serial Controller Drivers Overview](serial-drivers-overview.md)
    -   [Features of Serial and Serenum](features-of-serial-and-serenum.md)
    -   [Configuration of Serial Devices and Drivers](configuration-of-serial-devices-and-drivers.md)
    -   [Operation of Serenum and Serial](operation-of-serenum-and-serial.md)
    -   [Registry Settings for Serial](registry-settings-for-serial.md)
    -   [Registry Settings for Serenum](registry-settings-for-serenum.md)
    -   [Serial Driver Reference](https://msdn.microsoft.com/library/windows/hardware/ff547476)
    -   [Serenum Driver Reference](https://msdn.microsoft.com/library/windows/hardware/ff547040)
    -   Data definitions in the Ntddser.h header file in the WDK.

<!-- -->

-   Ports [device setup class](https://msdn.microsoft.com/library/windows/hardware/ff541509)

    The Ports class includes *serial ports* and *COM ports*. A serial port is a serial communication hardware interface on a 16550 UART or compatible device. An RS-232 port on a computer is typically a DB-9 or DB-25 connector that is electrically connected to the serial port on a UART. A COM port is a serial port that complies with additional Windows-specific requirements. For more information, see [Configuration of COM Ports](configuration-of-com-ports.md).

-   COM port [device interface class](https://msdn.microsoft.com/library/windows/hardware/ff541339)

    You must use a COM port device interface to access a COM port. (The GUID for the COM port device interface class is [**GUID\_DEVINTERFACE\_COMPORT**](https://msdn.microsoft.com/library/windows/hardware/ff545821).)

-   [COM port database](com-port-database.md) and [COM port database support routines](https://msdn.microsoft.com/library/windows/hardware/ff546483)

    The COM port database arbitrates the use of COM port numbers by COM ports.

For information about installing serial devices, see [Installing Serial Devices](installing-serial-devices.md).

For general information about the high-level operation of a serial device, see the information about the communications resources that are supported by the Windows Base Services in the Microsoft Windows SDK.

## Serial driver samples


These samples demonstrates serial drivers.

-   The [Serial](http://go.microsoft.com/fwlink/p/?LinkId=617962) sample builds a function driver for serial devices.
-   The [Serenum](http://go.microsoft.com/fwlink/p/?LinkId=617961) sample provides Plug and Play functionality of a bus driver for an RS-232 port.
-   A simple virtual serial driver (ComPort) and a controller-less modem driver (FakeModem).
    -   [The Virtual serial driver sample (UMDF 1.0)](http://go.microsoft.com/fwlink/p/?LinkId=617963)
    -   [The Virtual serial2 driver sample (KMDF)](http://go.microsoft.com/fwlink/p/?LinkId=722209)

 

 


--------------------
[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bserports\serports%5D:%20Using%20Serial.sys%20and%20Serenum.sys%20%20RELEASE:%20%288/4/2016%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")


