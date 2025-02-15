---
UID: NF:udecxusbdevice.UdecxUsbDeviceInitAddDescriptorWithIndex
title: UdecxUsbDeviceInitAddDescriptorWithIndex function (udecxusbdevice.h)
description: Learn how the UdecxUsbDeviceInitAddDescriptorWithIndex function adds a USB descriptor to the initialization parameters used to create a virtual USB device.
old-location: buses\udecxusbdeviceinitadddescriptorwithindex.htm
tech.root: usbref
ms.date: 05/07/2018
keywords: ["UdecxUsbDeviceInitAddDescriptorWithIndex function"]
ms.keywords: UdecxUsbDeviceInitAddDescriptorWithIndex, UdecxUsbDeviceInitAddDescriptorWithIndex function [Buses], buses.udecxusbdeviceinitadddescriptorwithindex, udecxusbdevice/UdecxUsbDeviceInitAddDescriptorWithIndex
req.header: udecxusbdevice.h
req.include-header: Udecx.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 1.15
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Udecxstub.lib
req.dll: 
req.irql: PASSIVE_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - UdecxUsbDeviceInitAddDescriptorWithIndex
 - udecxusbdevice/UdecxUsbDeviceInitAddDescriptorWithIndex
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Udecxstub.lib
 - Udecxstub.dll
api_name:
 - UdecxUsbDeviceInitAddDescriptorWithIndex
---

# UdecxUsbDeviceInitAddDescriptorWithIndex function


## -description

Adds a USB descriptor to the initialization parameters used to create a virtual USB device.

## -parameters

### -param UdecxUsbDeviceInit 

[in, out]
A pointer to a WDF-allocated structure that contains initialization parameters for the virtual USB device.  The client driver retrieved this pointer in the previous call to <a href="/windows-hardware/drivers/ddi/udecxusbdevice/nf-udecxusbdevice-udecxusbdeviceinitallocate">UdecxUsbDeviceInitAllocate</a>.

### -param Descriptor 

[in]
A caller-allocated buffer that contains the USB descriptor to add to the device.

### -param DescriptorLength 

[in]
The length of the descriptor buffer.

### -param DescriptorIndex 

[in]
The index of the descriptor.

## -returns

The method returns STATUS_SUCCESS if the operation succeeds. Otherwise, this method might return an appropriate <a href="/windows-hardware/drivers/kernel/ntstatus-values">NTSTATUS</a> error code.

## -see-also

<a href="/windows-hardware/drivers/usbcon/">Architecture: USB Device Emulation (UDE)</a>



<a href="/windows-hardware/drivers/usbcon/usb-string-descriptors">USB String Descriptors</a>



<a href="/windows-hardware/drivers/ddi/udecxusbdevice/nf-udecxusbdevice-udecxusbdeviceinitallocate">UdecxUsbDeviceInitAllocate</a>



<a href="/windows-hardware/drivers/usbcon/">Write a UDE client driver</a>
