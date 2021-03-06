---
title: Metadata
description: Metadata
ms.assetid: bab7803c-df1f-4282-a9d7-5536d30d00dc
---

# Metadata


The Metadata element specifies the namespaces of the XML schemas that are referenced in the service metadata package.

## <span id="Usage"></span><span id="usage"></span><span id="USAGE"></span>Usage


``` syntax
<Metadata
  MetadataID = "xs:anyURI">
  text
</Metadata>
```

## <span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes


<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribute</th>
<th>Type</th>
<th>Required</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>MetadataID</p></td>
<td><p>xs:anyURI</p></td>
<td><p>Yes</p></td>
<td><p>Specifies the namespace of an XML schema that is referenced within the service metadata package.</p></td>
</tr>
</tbody>
</table>

 

## <span id="Text_value"></span><span id="text_value"></span><span id="TEXT_VALUE"></span>Text value


The Uniform Resource Identifier (URI) of the namespace of a service metadata XML schema. The XML schema must be one of the schemas referenced within the services metadata package.

## <span id="Child_elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child elements


There are no child elements.

## <span id="Parent_elements"></span><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent elements


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[PackageStructure](packagestructure.md)</p></td>
<td><p>The [PackageStructure](packagestructure.md) element specifies the XML schemas which are referenced by the service metadata package.</p></td>
</tr>
</tbody>
</table>

 

## <span id="XSD"></span><span id="xsd"></span>XSD


``` syntax
<xs:element name="PackageStructure" type="tns:PackageStructureType" />

<xs:complexType name="PackageStructureType">
   <xs:sequence>
     <xs:element name="Metadata" type="tns:MetadataType" minOccurs="3" maxOccurs="unbounded" />
   </xs:sequence>
</xs:complexType>

<xs:complexType name="MetadataType">
  <xs:simpleContent>
    <xs:extension base="xs:string">
      <xs:attribute name="MetadataID" type="xs:anyURI" use="required" />
    </xs:extension>
  </xs:simpleContent>
</xs:complexType>
```

## <span id="Remarks"></span><span id="remarks"></span><span id="REMARKS"></span>Remarks


In the [PackageInfo](packageinfo.md) element, a minimum of two instances of the Metadata element must be specified. Each instance must specify the namespace of one of the following required XML schemas that are used to create a service metadata package:

-   [PackageInfo XML schema](packageinfo-xml-schema.md)

-   [ServiceInfo XML schema](serviceinfo-xml-schema.md)

-   [WindowsInfo XML schema](windowsinfo-xml-schema.md)

-   [SoftwareInfo XML schema](softwareinfo-xml-schema.md)

The easiest approach is to copy the following example above into your Packageinfo.xml file. If any of the folders specified above are not included in the service metadata package, make sure to remove the Metadata element from the [PackageStructure](packagestructure.md) element.

``` syntax
<PackageStructure>
  <Metadata MetadataID="http://schemas.microsoft.com/windows/DeviceMetadata/PackageInfo/2007/11">PackageInfo.xml</Metadata>
  <Metadata MetadataID="http://schemas.microsoft.com/windows/2010/05/DeviceMetadata/ServiceInfo">ServiceInformation</Metadata>
  <Metadata MetadataID="http://schemas.microsoft.com/windows/DeviceMetadata/WindowsInfo/2007/11/">WindowsInformation</Metadata>
  <Metadata MetadataID="http://schemas.microsoft.com/windows/2010/08/DeviceMetadata/SoftwareInfo">SoftwareInformation</Metadata>
</PackageStructure>
```

The SoftwareInformation folder and service metadata packages are not supported on devices running Windows 7.

Each folder name can be changed to an arbitrary name as long as the name is set in this metadata element. The following example shows how to use “WindowsInfo” as a folder name:

``` syntax
<Metadata MetadataID="http://schemas.microsoft.com/windows/DeviceMetadata/WindowsInfo/2007/11/">WindowsInfo</Metadata>
```

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bp_mb\p_mb%5D:%20Metadata%20%20RELEASE:%20%281/18/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")




