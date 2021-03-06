---
title: Renamed WHEA Data Types
author: windows-driver-content
description: Renamed WHEA Data Types
ms.assetid: e2c511a2-fd6e-4c7a-a47f-eb9b9f917bb4
keywords: ["Windows Hardware Error Architecture WDK , renamed data types", "WHEA WDK , renamed data types", "hardware errors WDK WHEA , renamed data types", "renamed data types WDK WHEA"]
---

# Renamed WHEA Data Types


Starting with the Windows 7 Windows Driver Kit (WDK), various WHEA data types have been renamed from earlier versions of the WDK. The majority of these changes were made so that the naming conventions in the WDK are consistent with the naming conventions of the *Common Platform Error Record* format. This format is described in Appendix N of version 2.2 of the [Unified Extensible Firmware Interface (UEFI) Specification](http://go.microsoft.com/fwlink/p/?linkid=69484).

The data types listed in this section have not been revised for Windows 7. For example, the list and types of members within a renamed structure have not changed, although the members themselves may have been renamed.

If you are developing new [platform-specific hardware error driver (PSHED) plug-ins](platform-specific-hardware-error-driver-plug-ins2.md), use the new WHEA data type names as defined in the Windows 7 and later versions of the WDK.

If you are building an existing PSHED plug-in with the Windows 7 and later versions of the WDK, you can still use the previous WHEA data type names. To do this, add the following to the *sources* file that is used to build the plug-in:

`C_DEFINES = $(C_DEFINES) /DWHEA_DOWNLEVEL_TYPE_NAMES`

However, for existing PSHED plug-ins, we strongly recommend that you rename the WHEA data types by using the names that are defined in the Windows 7 and later versions of the WDK.

The following tables list the WHEA data types' former and new names.

### <a href="" id="renamed-whea-globally-unique-identifiers--guids-"></a> Renamed WHEA Globally-Unique Identifiers (GUIDs)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Former name (WDK versions prior to Windows 7)</th>
<th>New name (Windows 7 WDK and later)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>IPF_PROCESSOR_SPECIFIC_SECTION_GUID</p></td>
<td><p>IPF_PROCESSOR_ERROR_SECTION_GUID</p></td>
</tr>
<tr class="even">
<td><p>IPF_SAL_RECORD_REFERENCE_SECTION_GUID</p></td>
<td><p>FIRMWARE_ERROR_RECORD_REFERENCE_GUID</p></td>
</tr>
<tr class="odd">
<td><p>PCIEXPRESS_SECTION_GUID</p></td>
<td><p>PCIEXPRESS_ERROR_SECTION_GUID</p></td>
</tr>
<tr class="even">
<td><p>PCIX_BUS_SECTION_GUID</p></td>
<td><p>PCIXBUS_ERROR_SECTION_GUID</p></td>
</tr>
<tr class="odd">
<td><p>PCIX_COMPONENT_SECTION_GUID</p></td>
<td><p>PCIXBUS_ERROR_SECTION_GUID</p></td>
</tr>
<tr class="even">
<td><p>PLATFORM_MEMORY_SECTION_GUID</p></td>
<td><p>MEMORY_ERROR_SECTION_GUID</p></td>
</tr>
<tr class="odd">
<td><p>PROCESSOR_GENERIC_SECTION_GUID</p></td>
<td><p>PROCESSOR_GENERIC_ERROR_SECTION_GUID</p></td>
</tr>
<tr class="even">
<td><p>X86_PROCESSOR_SPECIFIC_SECTION_GUID</p></td>
<td><p>XPF_PROCESSOR_ERROR_SECTION_GUID</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="renamed-whea-defines"></a> Renamed WHEA Defines

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Former name (WDK versions prior to Windows 7)</th>
<th>New name (Windows 7 WDK and later)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>WHEA_SECTION_DESCRIPTOR_REVISION</p></td>
<td><p>WHEA_ERROR_RECORD_SECTION_DESCRIPTOR_REVISION</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="renamed-whea-structures-and-unions"></a> Renamed WHEA Structures and Unions

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Former name (WDK versions prior to Windows 7)</th>
<th>New name (Windows 7 WDK and later)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>WHEA_FIRMWARE_RECORD</p></td>
<td><p>[<strong>WHEA_FIRMWARE_ERROR_RECORD_REFERENCE</strong>](https://msdn.microsoft.com/library/windows/hardware/ff560520)</p></td>
</tr>
<tr class="even">
<td><p>WHEA_GENERIC_PROCESSOR_ERROR</p></td>
<td><p>[<strong>WHEA_PROCESSOR_GENERIC_ERROR_SECTION</strong>](https://msdn.microsoft.com/library/windows/hardware/ff560607)</p></td>
</tr>
<tr class="odd">
<td><p>WHEA_GENERIC_PROCESSOR_ERROR_VALIDBITS</p></td>
<td><p>[<strong>WHEA_PROCESSOR_GENERIC_ERROR_SECTION_VALIDBITS</strong>](https://msdn.microsoft.com/library/windows/hardware/ff560610)</p></td>
</tr>
<tr class="even">
<td><p>WHEA_MEMORY_ERROR</p></td>
<td><p>[<strong>WHEA_MEMORY_ERROR_SECTION</strong>](https://msdn.microsoft.com/library/windows/hardware/ff560565)</p></td>
</tr>
<tr class="odd">
<td><p>WHEA_MEMORY_ERROR_VALIDBITS</p></td>
<td><p>[<strong>WHEA_MEMORY_ERROR_SECTION_VALIDBITS</strong>](https://msdn.microsoft.com/library/windows/hardware/ff560568)</p></td>
</tr>
<tr class="even">
<td><p>WHEA_NMI_ERROR</p></td>
<td><p>[<strong>WHEA_NMI_ERROR_SECTION</strong>](https://msdn.microsoft.com/library/windows/hardware/ff560571)</p></td>
</tr>
<tr class="odd">
<td><p>WHEA_PCIEXPRESS_ERROR</p></td>
<td><p>[<strong>WHEA_PCIEXPRESS_ERROR_SECTION</strong>](https://msdn.microsoft.com/library/windows/hardware/ff560576)</p></td>
</tr>
<tr class="even">
<td><p>WHEA_PCIEXPRESS_ERROR_VALIDBITS</p></td>
<td><p>[<strong>WHEA_PCIEXPRESS_ERROR_SECTION_VALIDBITS</strong>](https://msdn.microsoft.com/library/windows/hardware/ff560580)</p></td>
</tr>
<tr class="odd">
<td><p>WHEA_PCIXBUS_ERROR</p></td>
<td><p>[<strong>WHEA_PCIXBUS_ERROR_SECTION</strong>](https://msdn.microsoft.com/library/windows/hardware/ff560583)</p></td>
</tr>
<tr class="even">
<td><p>WHEA_PCIXBUS_ERROR_VALIDBITS</p></td>
<td><p>[<strong>WHEA_PCIXBUS_ERROR_SECTION_VALIDBITS</strong>](https://msdn.microsoft.com/library/windows/hardware/ff560585)</p></td>
</tr>
<tr class="odd">
<td><p>WHEA_PCIXDEVICE_ERROR</p></td>
<td><p>[<strong>WHEA_PCIXDEVICE_ERROR_SECTION</strong>](https://msdn.microsoft.com/library/windows/hardware/ff560589)</p></td>
</tr>
<tr class="even">
<td><p>WHEA_PCIXDEVICE_ERROR_VALIDBITS</p></td>
<td><p>[<strong>WHEA_PCIXDEVICE_ERROR_SECTION_VALIDBITS</strong>](https://msdn.microsoft.com/library/windows/hardware/ff560591)</p></td>
</tr>
<tr class="odd">
<td><p>WHEA_XPF_PROCESSOR_ERROR</p></td>
<td><p>[<strong>WHEA_XPF_PROCESSOR_ERROR_SECTION</strong>](https://msdn.microsoft.com/library/windows/hardware/ff560655)</p></td>
</tr>
<tr class="even">
<td><p>WHEA_XPF_PROCESSOR_ERROR_VALIDBITS</p></td>
<td><p>[<strong>WHEA_XPF_PROCESSOR_ERROR_SECTION_VALIDBITS</strong>](https://msdn.microsoft.com/library/windows/hardware/ff560657)</p></td>
</tr>
</tbody>
</table>

 

 

 


--------------------
[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bwhea\whea%5D:%20Renamed%20WHEA%20Data%20Types%20%20RELEASE:%20%289/14/2016%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")


