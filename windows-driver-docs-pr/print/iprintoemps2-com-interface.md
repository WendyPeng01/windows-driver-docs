---
title: IPrintOemPS2 COM Interface
author: windows-driver-content
description: IPrintOemPS2 COM Interface
ms.assetid: 6743d73e-243b-4a05-8e88-576c65b37a19
keywords: ["IPrintOemPS2"]
---

# IPrintOemPS2 COM Interface


## <a href="" id="ddk-iprintoemps2-com-interface-gg"></a>


The `IPrintOemPS2` COM interface contains all the methods of, and extends the capabilities of the [IPrintOemPS COM Interface](iprintoemps-com-interface.md). This interface is limited to Pscript5 rendering plug-ins that run on Windows XP and later versions of Windows operating system.

The following table lists and describes all of the methods provided by the `IPrintOemPS2` interface. Rendering plug-ins must define all the listed methods. If a method is not needed, it can simply return E\_NOTIMPL.

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
<td><p>[<strong>IPrintOemPS2::GetPDEVAdjustment</strong>](https://msdn.microsoft.com/library/windows/hardware/ff553189)</p></td>
<td><p>Enables a plug-in to override specific PDEV settings.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IPrintOemPS2::WritePrinter</strong>](https://msdn.microsoft.com/library/windows/hardware/ff553196)</p></td>
<td><p>Enables a plug-in to capture all output data generated by a Postscript driver.</p></td>
</tr>
</tbody>
</table>

 

For more information, see [Implementing Printer Driver COM Interfaces](implementing-printer-driver-com-interfaces.md).

 

 


--------------------
[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bprint\print%5D:%20IPrintOemPS2%20COM%20Interface%20%20RELEASE:%20%289/1/2016%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")


