---
UID: NF:ntifs.IoGetAttachedDeviceReference
title: IoGetAttachedDeviceReference function (ntifs.h)
description: The IoGetAttachedDeviceReference routine in ntifs.h returns a pointer to the highest level device object in a driver stack and increments the reference count.
old-location: kernel\iogetattacheddevicereference.htm
tech.root: kernel
ms.date: 04/30/2018
keywords: ["IoGetAttachedDeviceReference function"]
ms.keywords: IoGetAttachedDeviceReference, IoGetAttachedDeviceReference routine [Kernel-Mode Driver Architecture], k104_f7fa8878-306a-4de2-b418-8102754306f7.xml, kernel.iogetattacheddevicereference, wdm/IoGetAttachedDeviceReference
req.header: ntifs.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 2000.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: DanglingDeviceObjectReference, HwStorPortProhibitedDDIs
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: <= DISPATCH_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - IoGetAttachedDeviceReference
 - ntifs/IoGetAttachedDeviceReference
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - IoGetAttachedDeviceReference
---

# IoGetAttachedDeviceReference function (ntifs.h)


## -description

The <b>IoGetAttachedDeviceReference</b> routine returns a pointer to the highest level device object in a driver stack and increments the reference count on that object.

## -parameters

### -param DeviceObject 

[in]
Pointer to the device object for which the topmost attached device object is retrieved.

## -returns

<b>IoGetAttachedDeviceReference</b> returns a pointer to the highest level device object in a stack of attached device objects after incrementing the reference count on the object.

## -remarks

If the device object at <i>DeviceObject</i> has no device objects attached to it, <i>DeviceObject</i> and the returned pointer are equal.

Device driver writers must ensure that when they have completed all operations that required them to make this call, that they call <a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-obdereferenceobject">ObDereferenceObject</a> with the device object pointer returned by this routine. Failure to do so will prevent the system from freeing or deleting the device object because of an outstanding reference count.

## -see-also

<a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-obdereferenceobject">ObDereferenceObject</a>
