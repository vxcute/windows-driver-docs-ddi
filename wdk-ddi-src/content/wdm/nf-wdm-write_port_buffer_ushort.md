---
UID: NF:wdm.WRITE_PORT_BUFFER_USHORT
title: WRITE_PORT_BUFFER_USHORT function (wdm.h)
description: The WRITE_PORT_BUFFER_USHORT function (wdm.h) writes a number of USHORT values from a buffer to the specified port address.
old-location: kernel\write_port_buffer_ushort.htm
tech.root: kernel
ms.date: 04/30/2018
keywords: ["WRITE_PORT_BUFFER_USHORT function"]
ms.keywords: WRITE_PORT_BUFFER_USHORT, WRITE_PORT_BUFFER_USHORT routine [Kernel-Mode Driver Architecture], k103_c8549446-4478-4c5d-82c2-55e963c81cf3.xml, kernel.write_port_buffer_ushort, wdm/WRITE_PORT_BUFFER_USHORT
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
 - WRITE_PORT_BUFFER_USHORT
 - wdm/WRITE_PORT_BUFFER_USHORT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Hal.lib
 - Hal.dll
api_name:
 - WRITE_PORT_BUFFER_USHORT
---

# WRITE_PORT_BUFFER_USHORT function (wdm.h)


## -description

The <b>WRITE_PORT_BUFFER_USHORT</b> routine writes a number of USHORT values from a buffer to the specified port address.

## -parameters

### -param Port 

[in]
Pointer to the port, which must be a mapped memory range in I/O space.

### -param Buffer 

[in]
Pointer to a buffer from which an array of USHORT values is to be written.

### -param Count 

[in]
Specifies the number of USHORT values to be written to the port.

## -returns

None

## -remarks

The size of the buffer must be large enough to contain at least the specified number of USHORT values.

Callers of <b>WRITE_PORT_BUFFER_USHORT</b> can be running at any IRQL, assuming the <i>Buffer</i> is resident and the <i>Port</i> is resident, mapped device memory.

