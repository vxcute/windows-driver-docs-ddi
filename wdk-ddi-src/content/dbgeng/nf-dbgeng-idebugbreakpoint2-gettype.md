---
UID: NF:dbgeng.IDebugBreakpoint2.GetType
title: IDebugBreakpoint2::GetType (dbgeng.h)
description: The GetType method returns the type of the breakpoint and processor that a breakpoint is set for. This method belongs to the IDebugBreakpoint2 interface.
old-location: debugger\gettype.htm
tech.root: debugger
ms.date: 05/03/2018
keywords: ["IDebugBreakpoint2::GetType"]
ms.keywords: ComOther_3305c400-f816-463b-a643-4495bf546460.xml, GetType, GetType method [Windows Debugging], GetType method [Windows Debugging],IDebugBreakpoint interface, GetType method [Windows Debugging],IDebugBreakpoint2 interface, IDebugBreakpoint interface [Windows Debugging],GetType method, IDebugBreakpoint2 interface [Windows Debugging],GetType method, IDebugBreakpoint2.GetType, IDebugBreakpoint2::GetType, IDebugBreakpoint::GetType, dbgeng/IDebugBreakpoint2::GetType, dbgeng/IDebugBreakpoint::GetType, debugger.gettype
req.header: dbgeng.h
req.include-header: Dbgeng.h
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
 - IDebugBreakpoint2::GetType
 - dbgeng/IDebugBreakpoint2::GetType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dbgeng.h
api_name:
 - IDebugBreakpoint2::GetType
---

# IDebugBreakpoint2::GetType


## -description

The <b>GetType</b> method returns the type of the breakpoint and the type of the processor that a breakpoint is set for.

## -parameters

### -param BreakType 

[out]
The type of the breakpoint.  The type can be one of the following  values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>
DEBUG_BREAKPOINT_CODE

</td>
<td>
Software breakpoint

</td>
</tr>
<tr>
<td>
DEBUG_BREAKPOINT_DATA

</td>
<td>
Processor breakpoint

</td>
</tr>
</table>

### -param ProcType 

[out]
The type of the processor that the breakpoint is set for.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 

This method can also return error values.  For more information, see <a href="/windows-hardware/drivers/debugger/hresult-values">Return Values</a>.

## -remarks

If changes are made to the breakpoint, the processor type might change.

The <a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugbreakpoint2-getparameters">GetParameters</a> method also returns the information that is returned in <i>BreakType</i> and <i>ProcType</i>.

For more information about breakpoint types, see <a href="/windows-hardware/drivers/debugger/breakpoints3">Breakpoints</a>.

