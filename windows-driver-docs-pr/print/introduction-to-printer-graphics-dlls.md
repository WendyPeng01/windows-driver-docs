---
title: Introduction to Printer Graphics DLLs
author: windows-driver-content
description: Introduction to Printer Graphics DLLs
ms.assetid: 3f7ce476-6bef-4a80-ae2a-2a63e891dda1
keywords: ["printer graphics DLL WDK , about printer graphics DLL", "graphics DLL WDK printer , about printer graphics DLL", "graphics DLL WDK printer", "printer graphics DLL WDK"]
---

# Introduction to Printer Graphics DLLs


Printer graphics DLLs implement Drv-prefixed graphics DDI functions that are described in [Using the Graphics DDI](https://msdn.microsoft.com/library/windows/hardware/ff570139). These DLLs have the following two responsibilities:

-   Assist GDI in rendering a print job.

    A printer graphics DLL can provide graphics DDI drawing functions to handle drawing operations that must be performed in a device-specific manner and thus cannot be handled exclusively by GDI's rendering engine.

-   Deliver a rendered data stream to the spooler.

    Printer graphics DLLs typically produce an output stream in a [RAW data type](raw-data-type.md) (including command sequences) that the spooler can send to printer hardware through [*print monitors*](https://msdn.microsoft.com/library/windows/hardware/ff556325#wdkgloss-print-monitor).

The amount of rendering assistance that a printer graphics DLL must provide is printer type-specific, depending on the hardware's drawing capabilities, and includes the following scenarios:

-   The GDI rendering engine does all rendering, using a GDI-managed surface. The graphics DLL does not provide any DDI drawing functions.

-   The graphics DLL provides some graphics DDI drawing functions to work in conjunction with GDI's rendering engine, using a GDI-managed surface. The graphics DDI drawing functions provided by the graphics DLL can optionally call back to the GDI rendering engine's [GDI support services](https://msdn.microsoft.com/library/windows/hardware/ff566714).

-   The graphics DLL does all rendering by providing graphics DDI drawing functions and using a device-managed surface.

For example, the [Microsoft Universal Printer Driver](microsoft-universal-printer-driver.md) (Unidrv) uses a GDI-managed surface and provides some graphics DDI drawing functions, while the [Microsoft PostScript Printer Driver](microsoft-postscript-printer-driver.md) uses a device-managed surface.

For more information about providing rendering assistance in graphics drivers, see [Surface Types](https://msdn.microsoft.com/library/windows/hardware/ff569900) and [Using the Graphics DDI](https://msdn.microsoft.com/library/windows/hardware/ff570139).

The following two figures illustrate the data flow that occurs when an application creates a print job using GDI. EMF recording and playback are combined in these figures.

The first diagram depicts a user-mode printer graphics DLL.

**Note**   In Windows Vista printer graphics DLLs can only execute in user mode. For more information, see [Choosing User Mode or Kernel Mode](choosing-user-mode-or-kernel-mode.md).

 

![diagram illustrating a user-mode printer graphics dll](images/usrmdprt.png)

The second diagram depicts a kernel-mode printer graphics DLL.

![print job data flow, using a kernel-mode printer graphics dll](images/gdiprint.png)

Note in these diagrams that if the output format from GDI is [*enhanced metafile (EMF)*](https://msdn.microsoft.com/library/windows/hardware/ff556279#wdkgloss-enhanced-metafile--emf-), the printer graphics DLL does not receive the job until the EMF print processor plays back EMF records. Note also that the EMF Print Processor changes output format to non-EMF.

The diagrams illustrate an entirely local environment. If the printer is connected to a server, EMF records are typically produced by the client's copy of the GDI rendering engine (GRE) and then spooled to a local file that is sent to the server. The server's copy of the spooler reads the file and sends the records to the server's EMF print processor, and the server's copy of the GRE calls the server's printer graphics DLL.

 

 


--------------------
[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bprint\print%5D:%20Introduction%20to%20Printer%20Graphics%20DLLs%20%20RELEASE:%20%289/1/2016%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")


