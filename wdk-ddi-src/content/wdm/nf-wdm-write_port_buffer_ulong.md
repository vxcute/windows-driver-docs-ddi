---
UID: NF:wdm.WRITE_PORT_BUFFER_ULONG
title: WRITE_PORT_BUFFER_ULONG function (wdm.h)
description: The WRITE_PORT_BUFFER_ULONG function (wdm.h) writes a number of ULONG values from a buffer to the specified port address.
old-location: kernel\write_port_buffer_ulong.htm
tech.root: kernel
ms.date: 04/30/2018
keywords: ["WRITE_PORT_BUFFER_ULONG function"]
ms.keywords: WRITE_PORT_BUFFER_ULONG, WRITE_PORT_BUFFER_ULONG routine [Kernel-Mode Driver Architecture], k103_821262d5-40d2-435b-965e-cf0a917736b3.xml, kernel.write_port_buffer_ulong, wdm/WRITE_PORT_BUFFER_ULONG
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h, Miniport.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 2000.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Hal.lib
req.dll: 
req.irql: Any level (see Remarks section)
targetos: Windows
req.typenames: 
f1_keywords:
 - WRITE_PORT_BUFFER_ULONG
 - wdm/WRITE_PORT_BUFFER_ULONG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Hal.lib
 - Hal.dll
api_name:
 - WRITE_PORT_BUFFER_ULONG
---

# WRITE_PORT_BUFFER_ULONG function (wdm.h)


## -description

The <b>WRITE_PORT_BUFFER_ULONG</b> routine writes a number of ULONG values from a buffer to the specified port address.

## -parameters

### -param Port 

[in]
Pointer to the port, which must be a mapped memory range in I/O space.

### -param Buffer 

[in]
Pointer to a buffer from which an array of ULONG values is to be written.

### -param Count 

[in]
Specifies the number of ULONG values to be written to the port.

## -returns

None

## -remarks

The size of the buffer must be large enough to contain at least the specified number of ULONG values.

Callers of <b>WRITE_PORT_BUFFER_ULONG</b> can be running at any IRQL, assuming the <i>Buffer</i> is resident and the <i>Port</i> is resident, mapped device memory.

