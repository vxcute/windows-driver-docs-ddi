---
UID: NS:ntddndis._NDIS_OFFLOAD_PARAMETERS
title: _NDIS_OFFLOAD_PARAMETERS (ntddndis.h)
description: The NDIS_OFFLOAD_PARAMETERS structure specifies the current task offload configuration settings in response to an OID set request of OID_TCP_OFFLOAD_PARAMETERS.
old-location: netvista\ndis_offload_parameters.htm
tech.root: netvista
ms.date: 02/27/2020
ms.keywords: "*PNDIS_OFFLOAD_PARAMETERS, NDIS_ENCAPSULATION_TYPE_GRE_MAC, NDIS_OFFLOAD_PARAMETERS, NDIS_OFFLOAD_PARAMETERS structure [Network Drivers Starting with Windows Vista], NDIS_OFFLOAD_PARAMETERS_IPSECV1_AH_AND_ESP_ENABLED, NDIS_OFFLOAD_PARAMETERS_IPSECV1_AH_ENABLED, NDIS_OFFLOAD_PARAMETERS_IPSECV1_DISABLED, NDIS_OFFLOAD_PARAMETERS_IPSECV1_ESP_ENABLED, NDIS_OFFLOAD_PARAMETERS_IPSECV2_AH_AND_ESP_ENABLED, NDIS_OFFLOAD_PARAMETERS_IPSECV2_AH_ENABLED, NDIS_OFFLOAD_PARAMETERS_IPSECV2_DISABLED, NDIS_OFFLOAD_PARAMETERS_IPSECV2_ESP_ENABLED, NDIS_OFFLOAD_PARAMETERS_LSOV1_DISABLED, NDIS_OFFLOAD_PARAMETERS_LSOV1_ENABLED, NDIS_OFFLOAD_PARAMETERS_LSOV2_DISABLED, NDIS_OFFLOAD_PARAMETERS_LSOV2_ENABLED, NDIS_OFFLOAD_PARAMETERS_NO_CHANGE, NDIS_OFFLOAD_PARAMETERS_REVISION_1, NDIS_OFFLOAD_PARAMETERS_REVISION_2, NDIS_OFFLOAD_PARAMETERS_REVISION_3, NDIS_OFFLOAD_PARAMETERS_RSC_DISABLED, NDIS_OFFLOAD_PARAMETERS_RSC_ENABLED, NDIS_OFFLOAD_SET_NO_CHANGE, NDIS_OFFLOAD_SET_OFF, NDIS_OFFLOAD_SET_ON, PNDIS_OFFLOAD_PARAMETERS, PNDIS_OFFLOAD_PARAMETERS structure pointer [Network Drivers Starting with Windows Vista], _NDIS_OFFLOAD_PARAMETERS, netvista.ndis_offload_parameters, ntddndis/NDIS_OFFLOAD_PARAMETERS, ntddndis/PNDIS_OFFLOAD_PARAMETERS, tcpip_offload_ref_9ae50974-12a7-4c63-973e-27684a4f1474.xml"
req.header: ntddndis.h
req.include-header: Ndis.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista,Supported in NDIS 6.0 and later.
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NDIS_OFFLOAD_PARAMETERS, *PNDIS_OFFLOAD_PARAMETERS
f1_keywords:
 - _NDIS_OFFLOAD_PARAMETERS
 - ntddndis/_NDIS_OFFLOAD_PARAMETERS
 - PNDIS_OFFLOAD_PARAMETERS
 - ntddndis/PNDIS_OFFLOAD_PARAMETERS
 - NDIS_OFFLOAD_PARAMETERS
 - ntddndis/NDIS_OFFLOAD_PARAMETERS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddndis.h
api_name:
 - _NDIS_OFFLOAD_PARAMETERS
 - PNDIS_OFFLOAD_PARAMETERS
 - NDIS_OFFLOAD_PARAMETERS
---

# _NDIS_OFFLOAD_PARAMETERS structure


## -description

The <b>NDIS_OFFLOAD_PARAMETERS</b> structure specifies the current task offload configuration settings in
  response to an 
  OID set request of <a href="/windows-hardware/drivers/network/oid-tcp-offload-parameters">OID_TCP_OFFLOAD_PARAMETERS</a>.

## -struct-fields

### -field Header

The 
     <a href="/windows-hardware/drivers/ddi/content/objectheader/ns-objectheader-ndis_object_header">NDIS_OBJECT_HEADER</a> structure for the
     <b>NDIS_OFFLOAD_PARAMETERS</b> structure. Set the 
     <b>Type</b> member of the structure that 
     <b>Header</b> specifies to NDIS_OBJECT_TYPE_DEFAULT.

To indicate the version of the <b>NDIS_OFFLOAD_PARAMETERS</b> structure, set the 
     <b>Revision</b> member to one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_REVISION_3"></a><a id="ndis_offload_parameters_revision_3"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_REVISION_3</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Supports the 
        <b>RscIPv4</b> , <b>RscIPv6</b>, <b>EncapsulatedPacketTaskOffload</b>, and   <b>EncapsulationTypes</b> members for NDIS 6.30.

Set the 
        <b>Size</b> member to NDIS_SIZEOF_OFFLOAD_PARAMETERS_REVISION_3.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_REVISION_2"></a><a id="ndis_offload_parameters_revision_2"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_REVISION_2</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Supports the 
        <b>IPsecV2</b>, 
        <b>IPsecV2IPv4</b>, 
        <b>Reserved1</b>, and 
        <b>Reserved2</b> members for NDIS 6.1.

Set the 
        <b>Size</b> member to NDIS_SIZEOF_OFFLOAD_PARAMETERS_REVISION_2.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_REVISION_1"></a><a id="ndis_offload_parameters_revision_1"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_REVISION_1</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Original version for NDIS 6.0.

Set the 
        <b>Size</b> member to NDIS_SIZEOF_OFFLOAD_PARAMETERS_REVISION_1.

</td>
</tr>
</table>

### -field IPv4Checksum

The IPv4 checksum setting of the miniport adapter. For more information, see the following Remarks
     section.

### -field TCPIPv4Checksum

The IPv4 checksum setting of the miniport adapter for TCP packets. For more information, see the
     following Remarks section.

### -field UDPIPv4Checksum

The IPv4 checksum setting of the miniport adapter for UDP packets. For more information, see the
     following Remarks section.

### -field TCPIPv6Checksum

The IPv6 checksum setting of the miniport adapter for TCP packets. For more information, see the
     following Remarks section.

### -field UDPIPv6Checksum

The IPv6 checksum setting of the miniport adapter for UDP packets. For more information, see the
     following Remarks section.

### -field LsoV1

The large send offload version 1 (LSOV1) setting of the miniport adapter. This setting should be
     one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_NO_CHANGE"></a><a id="ndis_offload_parameters_no_change"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_NO_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
The miniport driver should not change the current setting.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_LSOV1_DISABLED"></a><a id="ndis_offload_parameters_lsov1_disabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_LSOV1_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
LSOV1 is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_LSOV1_ENABLED"></a><a id="ndis_offload_parameters_lsov1_enabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_LSOV1_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
LSOV1 is enabled.

</td>
</tr>
</table>

### -field IPsecV1

The Internet protocol security (IPsec) offload setting of the miniport adapter. This setting
     should be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_NO_CHANGE"></a><a id="ndis_offload_parameters_no_change"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_NO_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
The miniport driver should not change the current setting.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_IPSECV1_DISABLED"></a><a id="ndis_offload_parameters_ipsecv1_disabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_IPSECV1_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
IPsec offload is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_IPSECV1_AH_ENABLED"></a><a id="ndis_offload_parameters_ipsecv1_ah_enabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_IPSECV1_AH_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
The IPsec offload Authentication Header (AH) feature should be enabled for transmit and
       receive.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_IPSECV1_ESP_ENABLED"></a><a id="ndis_offload_parameters_ipsecv1_esp_enabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_IPSECV1_ESP_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
The IPsec offload Encapsulating Security Payload (ESP) feature should be enabled for transmit
       and receive.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_IPSECV1_AH_AND_ESP_ENABLED"></a><a id="ndis_offload_parameters_ipsecv1_ah_and_esp_enabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_IPSECV1_AH_AND_ESP_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
The IPsec offload AH and ESP features areenabled for transmit and receive.

</td>
</tr>
</table>

### -field LsoV2IPv4

The IPv4 large send offload version 2 (LSOV2) setting of the miniport adapter. This setting should
     be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_NO_CHANGE"></a><a id="ndis_offload_parameters_no_change"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_NO_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
The miniport driver should not change the current setting.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_LSOV2_DISABLED"></a><a id="ndis_offload_parameters_lsov2_disabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_LSOV2_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
LSOV2 for IPv4 is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_LSOV2_ENABLED"></a><a id="ndis_offload_parameters_lsov2_enabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_LSOV2_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
LSOV2 for IPv4 is enabled.

</td>
</tr>
</table>

### -field LsoV2IPv6

The IPv6 LSOV2 setting of the miniport adapter. These settings are specified as one of the
     following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_NO_CHANGE"></a><a id="ndis_offload_parameters_no_change"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_NO_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
The miniport driver should not change the current setting.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_LSOV2_DISABLED"></a><a id="ndis_offload_parameters_lsov2_disabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_LSOV2_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
LSOV2 for IPv6 is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_LSOV2_ENABLED"></a><a id="ndis_offload_parameters_lsov2_enabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_LSOV2_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
LSOV2 for IPv6 is enabled.

</td>
</tr>
</table>

### -field TcpConnectionIPv4

The IPv4 connection offload setting of the miniport adapter. These settings are specified as one
     of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_NO_CHANGE"></a><a id="ndis_offload_parameters_no_change"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_NO_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
The miniport driver should not change the current setting.

</td>
</tr>
</table>

### -field TcpConnectionIPv6

The IPv6 connection offload setting of the miniport adapter. These settings are specified as one
     of the following values:
     

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_NO_CHANGE"></a><a id="ndis_offload_parameters_no_change"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_NO_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
The miniport driver should not change the current setting.

</td>
</tr>
</table>

### -field Flags

A set of flags that can be combined with a bitwise OR operation. Set this member to zero. There
     are currently no flags defined.

### -field IPsecV2

The Internet protocol security (IPsec) offload version 2 setting of a miniport adapter that supports
      IPv6 and IPv4. This member specifies the setting for both IPv6 and IPv4 support. This setting should be
      one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_NO_CHANGE"></a><a id="ndis_offload_parameters_no_change"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_NO_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
The miniport driver should not change the current setting.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_IPSECV2_DISABLED"></a><a id="ndis_offload_parameters_ipsecv2_disabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_IPSECV2_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
IPsec offload version 2 is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_IPSECV2_AH_ENABLED"></a><a id="ndis_offload_parameters_ipsecv2_ah_enabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_IPSECV2_AH_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
The IPsec offload version 2 Authentication Header (AH) feature should be enabled for transmit
        and receive.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_IPSECV2_ESP_ENABLED"></a><a id="ndis_offload_parameters_ipsecv2_esp_enabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_IPSECV2_ESP_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
The IPsec offload version 2 Encapsulating Security Payload (ESP) feature should be enabled for
        transmit and receive.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_IPSECV2_AH_AND_ESP_ENABLED"></a><a id="ndis_offload_parameters_ipsecv2_ah_and_esp_enabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_IPSECV2_AH_AND_ESP_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
The IPsec offload version 2A H and ESP features are enabled for transmit and receive.

</td>
</tr>
</table>

### -field IPsecV2IPv4

The Internet protocol security (IPsec) offload version 2 setting of a miniport adapter that supports
      IPv4 and does not support IPv6. If the miniport driver supports IPv6, the 
      <b>IPsecV2</b> member specifies the IPv4 setting and this member is not used. This setting should be one
      of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_NO_CHANGE"></a><a id="ndis_offload_parameters_no_change"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_NO_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
The miniport driver should not change the current setting.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_IPSECV2_DISABLED"></a><a id="ndis_offload_parameters_ipsecv2_disabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_IPSECV2_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
IPsec offload version 2 is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_IPSECV2_AH_ENABLED"></a><a id="ndis_offload_parameters_ipsecv2_ah_enabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_IPSECV2_AH_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
The IPsec offload version 2 Authentication Header (AH) feature should be enabled for transmit
        and receive.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_IPSECV2_ESP_ENABLED"></a><a id="ndis_offload_parameters_ipsecv2_esp_enabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_IPSECV2_ESP_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
The IPsec offload version 2 Encapsulating Security Payload (ESP) feature should be enabled for
        transmit and receive.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_IPSECV2_AH_AND_ESP_ENABLED"></a><a id="ndis_offload_parameters_ipsecv2_ah_and_esp_enabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_IPSECV2_AH_AND_ESP_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
The IPsec offload version 2A H and ESP features are enabled for transmit and receive.

</td>
</tr>
</table>

### -field RscIPv4

Indicates Receive Segment Coalescing state for IPv4.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_NO_CHANGE"></a><a id="ndis_offload_parameters_no_change"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_NO_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
The RSC state is unchanged.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_RSC_ENABLED"></a><a id="ndis_offload_parameters_rsc_enabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_RSC_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
The RSC state is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_RSC_DISABLED"></a><a id="ndis_offload_parameters_rsc_disabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_RSC_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
The RSC state is disabled.

</td>
</tr>
</table>

### -field RscIPv6

Indicates Receive Segment Coalescing state for IPv6.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_NO_CHANGE"></a><a id="ndis_offload_parameters_no_change"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_NO_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
The RSC state is unchanged.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_RSC_ENABLED"></a><a id="ndis_offload_parameters_rsc_enabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_RSC_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
The RSC state is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_RSC_DISABLED"></a><a id="ndis_offload_parameters_rsc_disabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_RSC_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
The RSC state is disabled.

</td>
</tr>
</table>

### -field EncapsulatedPacketTaskOffload

A protocol driver sets <b>EncapsulatedPacketTaskOffload</b> as follows: 

<div class="alert"><b>Note</b>  For receive side offloads such as VMQ and RSS, there are other set OIDs that the protocol driver sends down to enable and configure the offload parameters (for example, queues, hash, and indirection table). The <b>EncapsulatedPacketTaskOffload</b> member is supplemental to those OIDs and instructs the NIC to also do these offloads for encapsulated packets.</div>
<div> </div>
<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_SET_NO_CHANGE"></a><a id="ndis_offload_set_no_change"></a><dl>
<dt><b>NDIS_OFFLOAD_SET_NO_CHANGE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The NVGRE task offload state is unchanged.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_SET_ON"></a><a id="ndis_offload_set_on"></a><dl>
<dt><b>NDIS_OFFLOAD_SET_ON</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Enables NVGRE task offloads.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_SET_OFF"></a><a id="ndis_offload_set_off"></a><dl>
<dt><b>NDIS_OFFLOAD_SET_OFF</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Disables NVGRE task offloads.

</td>
</tr>
</table>

### -field EncapsulationTypes

This field is effective only when the <b>EncapsulatedPacketTaskOffload</b> is set to <b>NDIS_OFFLOAD_SET_ON</b>. If the <b>EncapsulatedPacketTaskOffload</b> member is not set to <b>NDIS_OFFLOAD_SET_ON</b>, this member is zero. A protocol driver must set <b>EncapsulationTypes</b> to the bitwise OR of the flags corresponding to encapsulation types that it requires. It can select flags from the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NDIS_ENCAPSULATION_TYPE_GRE_MAC"></a><a id="ndis_encapsulation_type_gre_mac"></a><dl>
<dt><b>NDIS_ENCAPSULATION_TYPE_GRE_MAC</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Specifies GRE MAC  encapsulation (NVGRE).

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_ENCAPSULATION_TYPE_GRE_MAC"></a><a id="ndis_encapsulation_type_gre_mac"></a><dl>
<dt><b>NDIS_ENCAPSULATION_TYPE_VXLAN</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Specifies VXLAN encapsulation.

</td>
</tr>
</table>

### -field EncapsulationProtocolParameters

A union that describes the encapsulation parameters for VXLAN encapsulation. 

If the miniport driver advertised **VxlanUDPPortNumerConfigurable** as **TRUE**, then a protocol driver can set **EncapsulationProtocolParameters.VxlanParameters.VxlanUDPPortNumber** to a non-0 value. The minport driver must use this port number for matching and generating VXLAN frames after succeeding the OID, and also advertise the updated value in its capabilities. If the protocol driver passes a value of **0**, then the miniport driver continues to use the port number initialized from the standardized keyword.

### -field EncapsulationProtocolParameters.VxlanParameters

A structure that contains the **VxlanUDPPortNumber**.

### -field EncapsulationProtocolParameters.VxlanParameters.VxlanUDPPortNumber

The VXLAN destination port value. This value is set to the IANA-assigned value of 4789 by default. If the miniport driver supports a configurable port number as advertised in the [**NDIS_OFFLOAD**](../ntddndis/ns-ntddndis-_ndis_offload.md) structure, a protocol driver can issue an [OID_TCP_OFFLOAD_PARAMETERS](/windows-hardware/drivers/network/oid-tcp-offload-parameters) OID to enable NDIS_ENCAPSULATION_TYPE_VXLAN with a different value in **VxlanUDPPortNumber**. The miniport driver must use **VxlanUDPPortNumber** to determine VXLAN encapsulated packets for performing receive offloads.

### -field EncapsulationProtocolParameters.Value

The port value if **EncapsulationTypes** is not set to NDIS_ENCAPSULATION_TYPE_VXLAN.

### -field _ENCAPSULATION_PROTOCOL_PARAMETERS

The type name for **EncapsulationProtocolParameters**.

### -field UdpSegmentation

A structure that describes the miniport adapter's UDP Segmentation Offload (USO) settings.

### -field UdpSegmentation.IPv4

The IPv4 UDP Segmentation Offload (USO) setting of the miniport adapter. This setting should be one of the following values:     

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_NO_CHANGE"></a><a id="ndis_offload_parameters_no_change"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_NO_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
The miniport driver should not change the current setting.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_UDP_SEG_DISABLED"></a><a id="ndis_offload_parameters_udp_seg_disabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_UDP_SEG_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
USO is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_UDP_SEG_ENABLED"></a><a id="ndis_offload_parameters_udp_seg_enabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_UDP_SEG_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
USO is enabled.

</td>
</tr>
</table>

### -field UdpSegmentation.IPv6

The IPv6 UDP Segmentation Offload (USO) setting of the miniport adapter. This setting should be one of the following values:     

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_NO_CHANGE"></a><a id="ndis_offload_parameters_no_change"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_NO_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
The miniport driver should not change the current setting.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_UDP_SEG_DISABLED"></a><a id="ndis_offload_parameters_udp_seg_disabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_UDP_SEG_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
USO is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="NDIS_OFFLOAD_PARAMETERS_UDP_SEG_ENABLED"></a><a id="ndis_offload_parameters_udp_seg_enabled"></a><dl>
<dt><b>NDIS_OFFLOAD_PARAMETERS_UDP_SEG_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
USO is enabled.

</td>
</tr>
</table>

## -remarks

In response to an 
    <a href="/windows-hardware/drivers/network/oid-tcp-offload-parameters">OID_TCP_OFFLOAD_PARAMETERS</a> OID set
    request, a miniport driver uses the settings in the <b>NDIS_OFFLOAD_PARAMETERS</b> structure to set the current
    configuration of the miniport adapter.

NDIS retains the requested settings in the registry in the offload standardized keywords. When NDIS
    restarts the miniport adapter, the miniport driver reads the offload standardized keywords and uses them
    to set the default offload configuration of the NIC.

To access the checksum offload settings, use the following members of the <b>NDIS_OFFLOAD_PARAMETERS</b>
    structure:

<b>IPv4Checksum</b>

<b>TCPIPv4Checksum</b>

<b>UDPIPv4Checksum</b>

<b>TCPIPv6Checksum</b>

<b>UDPIPv6Checksum</b>

The preceding members can have one of the following values:

NDIS_OFFLOAD_PARAMETERS_NO_CHANGE  
The miniport driver should not change the current setting.

NDIS_OFFLOAD_PARAMETERS_TX_RX_DISABLED  
The feature that the member specifies is disabled.

NDIS_OFFLOAD_PARAMETERS_TX_ENABLED_RX_DISABLED  
The feature that the member specifies is enabled for transmit and disabled for receive.

NDIS_OFFLOAD_PARAMETERS_RX_ENABLED_TX_DISABLED  
The feature that the member specifies is enabled for receive and disabled for transmit.

NDIS_OFFLOAD_PARAMETERS_TX_RX_ENABLED  
The feature that the member specifies is enabled for transmit and receive.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/objectheader/ns-objectheader-ndis_object_header">NDIS_OBJECT_HEADER</a>



<a href="/windows-hardware/drivers/network/oid-tcp-connection-offload-hardware-capabilities">
   OID_TCP_OFFLOAD_HARDWARE_CAPABILITIES</a>



<a href="/windows-hardware/drivers/network/oid-tcp-offload-parameters">OID_TCP_OFFLOAD_PARAMETERS</a>

