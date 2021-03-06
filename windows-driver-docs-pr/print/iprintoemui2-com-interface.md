---
title: IPrintOemUI2 COM Interface
author: windows-driver-content
description: IPrintOemUI2 COM Interface
ms.assetid: 9aee61af-e8e2-4bc4-a17b-783242d1ac1f
keywords: ["IPrintOemUI2"]
---

# IPrintOemUI2 COM Interface


## <a href="" id="ddk-iprintoemui2-com-interface-gg"></a>


The `IPrintOemUI2` COM interface extends the [IPrintOemUI COM interface](iprintoemui-com-interface.md). In addition to all the methods in the **IPrintOemUI** interface, the `IPrintOemUI2` interface provides the following methods.

**Note**  If you are using the Windows Vista version of the Unidrv and Pscript DLLs, you can implement the following methods in Unidrv or Pscript5 plug-ins that run on Windows XP and later versions of Windows operating systems. Previous versions of the DLLs support the **IPrintOEM2::HideStandardUI** method in Pscript5 plug-ins only.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Method</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[<strong>IPrintOemUI2::DocumentEvent</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554141)</p></td>
<td><p>Enables a UI plug-in to replace the core driver UI module's default implementation of the [<strong>DrvDocumentEvent</strong>](https://msdn.microsoft.com/library/windows/hardware/ff548544) DDI.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IPrintOemUI2::HideStandardUI</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554142)</p></td>
<td><p>Enables a UI plug-in to specify whether the standard property sheets should be displayed or hidden.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>IPrintOemUI2::QueryJobAttributes</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554146)</p></td>
<td><p>Enables a UI plug-in to post-process the core driver's results after a call to the [<strong>DrvQueryJobAttributes</strong>](https://msdn.microsoft.com/library/windows/hardware/ff548581) DDI.</p></td>
</tr>
</tbody>
</table>

 

For more information, see [Implementing Printer Driver COM Interfaces](implementing-printer-driver-com-interfaces.md).

 

 


--------------------
[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bprint\print%5D:%20IPrintOemUI2%20COM%20Interface%20%20RELEASE:%20%289/1/2016%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")


