---
UID: NF:wdtfpnpaction.IWDTFPNPActions2.EnableDevice
title: IWDTFPNPActions2::EnableDevice (wdtfpnpaction.h)
description: Learn how the method enables the target device.
old-location: dtf\iwdtfpnpactions2_enabledevice.htm
tech.root: dtf
ms.date: 04/04/2018
keywords: ["IWDTFPNPActions2::EnableDevice"]
ms.keywords: EnableDevice, EnableDevice method [Windows Device Testing Framework], EnableDevice method [Windows Device Testing Framework],IWDTFPNPActions2 interface, IWDTFPNPActions2 interface [Windows Device Testing Framework],EnableDevice method, IWDTFPNPActions2.EnableDevice, IWDTFPNPActions2::EnableDevice, dtf.iwdtfpnpactions2_enabledevice, wdtfpnpaction/IWDTFPNPActions2::EnableDevice
req.header: wdtfpnpaction.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WDTFPNPAction.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - IWDTFPNPActions2::EnableDevice
 - wdtfpnpaction/IWDTFPNPActions2::EnableDevice
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wdtfpnpaction.h
api_name:
 - IWDTFPNPActions2::EnableDevice
---

# IWDTFPNPActions2::EnableDevice


## -description

Enables the target device.

## -parameters

### -param pbRebootRequired 

[out, retval]
True if the operation requires a restart to complete; otherwise, false.

## -returns

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

