---
UID: NF:wdm.RtlStoreUlongPtr
tech.root: 
title: RtlStoreUlongPtr
ms.date: 07/16/2021
targetos: Windows
description: "Learn more about: RtlStoreUlongPtr"
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wdm.h
req.idl: 
req.include-header: 
req.irql: Any level (see Remarks)
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wdm.h
api_name:
 - RtlStoreUlongPtr
f1_keywords:
 - RtlStoreUlongPtr
 - wdm/RtlStoreUlongPtr
dev_langs:
 - c++
---

## -description

The **RtlStoreUlongPtr** macro stores a specified ULONG_PTR value at a specified memory location, avoiding memory alignment faults.

## -parameters

### -param ADDRESS

[out]
A pointer to a location in which to store the ULONG_PTR value.

### -param VALUE

[in]
Specifies the ULONG_PTR value to be stored.

## -remarks

**RtlStoreUlongPtr** avoids memory alignment faults. If the value of _Address_ is not aligned to the storage requirements of a ULONG_PTR, **RtlStoreUlongPtr** stores the bytes of _Value_ beginning at the memory location (PUCHAR)_Address_.

**RtlStoreUlongPtr** runs at any IRQL if _Address_ points to nonpaged pool; otherwise it must run at IRQL <= APC_LEVEL.
