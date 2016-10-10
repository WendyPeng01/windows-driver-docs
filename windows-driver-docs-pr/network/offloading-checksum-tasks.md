---
title: Offloading Checksum Tasks
description: Offloading Checksum Tasks
ms.assetid: 5fb2f379-c357-4ec3-b103-bdbe23fcc033
keywords: ["task offload WDK TCP/IP transport , checksum tasks", "checksum tasks WDK networking"]
---

# Offloading Checksum Tasks


## <a href="" id="ddk-offloading-checksum-tasks-ng"></a>


NDIS supports offloading TCP/IP checksum tasks at run time.

**Note**  Checksum offload out-of-band (OOB) data is stored in the [**NET\_BUFFER\_LIST**](https://msdn.microsoft.com/library/windows/hardware/ff568388) information array. For more information about OOB data, see [Accessing TCP/IP Offload NET\_BUFFER\_LIST Information](accessing-tcp-ip-offload-net-buffer-list-information.md).

 

Before passing to the miniport driver a NET\_BUFFER\_LIST structure for a packet on which the miniport driver will perform checksum tasks, the TCP/IP transport specifies the checksum information that is associated with the NET\_BUFFER\_LIST structure. This information is specified by an [**NDIS\_TCP\_IP\_CHECKSUM\_NET\_BUFFER\_LIST\_INFO**](https://msdn.microsoft.com/library/windows/hardware/ff567877) structure, which is part of the NET\_BUFFER\_LIST information (out-of-band data) that is associated with the NET\_BUFFER\_LIST structure.

Before offloading the checksum calculation for a TCP packet, the TCP/IP transport calculates the one's complement sum for the TCP pseudoheader. The TCP/IP transport calculates the one's complement sum across all fields in the pseudoheader, including Source IP Address, Destination IP Address, Protocol, and the TCP length for TCP packets. The TCP/IP transport enters the one's complement sum for the pseudoheader in the Checksum field of the TCP header.

The one's complement sum for the pseudoheader provided by the TCP/IP transport gives the NIC an early start in calculating the real TCP checksum for the send packet. To calculate the actual TCP checksum, the NIC calculates the variable part of the TCP checksum (for the TCP header and payload), adds this checksum to the one's complement sum for the pseudoheader calculated by the TCP/IP transport, and calculates the 16-bit one's complement for the checksum. For more information about calculating such checksums, see RFC 793 and RFC 1122.

Note that the TCP/IP transport always ensures that the checksum field in the IP header of a packet is set to zero before passing the packet to an underlying miniport driver. The miniport driver should ignore the checksum field in an IP header. The miniport driver does not need to verify that the checksum field is set to zero and does not need to set this field to zero.

After it receives the NET\_BUFFER\_LIST structure in its [*MiniportSendNetBufferLists*](https://msdn.microsoft.com/library/windows/hardware/ff559440) or [**MiniportCoSendNetBufferLists**](https://msdn.microsoft.com/library/windows/hardware/ff559365) function, a miniport driver typically does the following checksum processing:

1.  The miniport driver calls the [**NET\_BUFFER\_LIST\_INFO**](https://msdn.microsoft.com/library/windows/hardware/ff568401) macro with an *\_Id* of **TcpIpChecksumNetBufferListInfo** to obtain an [**NDIS\_TCP\_IP\_CHECKSUM\_NET\_BUFFER\_LIST\_INFO**](https://msdn.microsoft.com/library/windows/hardware/ff567877) structure.

2.  The miniport driver tests the **IsIPv4** and **IsIPv6** flags in the NDIS\_TCP\_IP\_CHECKSUM\_NET\_BUFFER\_LIST\_INFO structure. If both the **IsIPv4** and **IsIPv6** flags are not set, the NIC should not perform any checksum operations on the packet.

3.  If the **IsIPv4** or **IsIPv6** flag is set, the miniport driver tests the **TcpChecksum**, **UdpChecksum**, and **IpHeaderChecksum** flags to determine which checksums the NIC should calculate for the packet.

4.  The miniport driver passes the packet to the NIC, which calculates the appropriate checksums for the packet. If a packet has both a tunnel IP header and a transport IP header, a NIC that supports IP checksum offloads performs IP checksum tasks only on the tunnel header. The TCP/IP transport performs IP checksum tasks on the transport IP header.

Before indicating a [**NET\_BUFFER\_LIST**](https://msdn.microsoft.com/library/windows/hardware/ff568388) structure for a receive packet on which it performs checksum tasks, the miniport driver validates the appropriate checksums and sets the appropriate *Xxx***ChecksumFailed** or *Xxx***ChecksumSucceeded** flags in the NDIS\_TCP\_IP\_CHECKSUM\_NET\_BUFFER\_LIST\_INFO structure.

 

 




