---
UID: NF:wiautil.wiauRegGetStrW
title: wiauRegGetStrW function (wiautil.h)
description: Learn how the wiauRegGetStr function gets a string value from the DeviceData section of the registry.
old-location: image\wiaureggetstr.htm
tech.root: image
ms.date: 05/03/2018
keywords: ["wiauRegGetStrW function"]
ms.keywords: image.wiaureggetstr, wiauFncs_b9145502-734d-40de-8086-c1f193966269.xml, wiauRegGetStr, wiauRegGetStr function [Imaging Devices], wiauRegGetStrA, wiauRegGetStrW, wiautil/wiauRegGetStr
req.header: wiautil.h
req.include-header: Wiautil.h
req.target-type: Desktop
req.target-min-winverclnt: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - wiauRegGetStrW
 - wiautil/wiauRegGetStrW
 - wiauRegGetStr
 - wiautil/wiauRegGetStr
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wiautil.h
api_name:
 - wiauRegGetStrW
 - wiauRegGetStr
---

# wiauRegGetStrW function


## -description

The <b>wiauRegGetStr</b> function gets a string value from the <b>DeviceData</b> section of the registry.

## -parameters

### -param hkKey 

[in]
Specifies the registry key handle. This parameter should be set to the value pointed to by the <i>phkeyDeviceData </i>parameter when <a href="/windows-hardware/drivers/ddi/wiautil/nf-wiautil-wiauregopendataw">wiauRegOpenData</a> returns.


#### - pwszValueName [in]

Points to the first character of a Unicode string containing the name of the registry entry.


#### - pwszValue [out]

Pointer to a memory location that receives the string value, including a terminating null character.

### -param pdwLength 

[in, out]
Pointer to a memory location that receives the length, in bytes, of the string value pointed to by the <i>pwszValue</i> parameter. The length includes the terminating null character.

## -returns

On success, the function returns S_OK. If the function fails, it returns a standard COM error.

## -see-also

<a href="/windows-hardware/drivers/ddi/wiautil/nf-wiautil-wiaureggetdwordw">wiauRegGetDword</a>



<a href="/windows-hardware/drivers/ddi/wiautil/nf-wiautil-wiauregopendataw">wiauRegOpenData</a>

