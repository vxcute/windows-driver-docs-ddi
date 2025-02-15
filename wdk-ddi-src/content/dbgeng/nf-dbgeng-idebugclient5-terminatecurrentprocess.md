---
UID: NF:dbgeng.IDebugClient5.TerminateCurrentProcess
title: IDebugClient5::TerminateCurrentProcess (dbgeng.h)
description: The TerminateCurrentProcess method attempts to terminate the current process. This method belongs to the IDebugClient5 interface.
old-location: debugger\terminatecurrentprocess.htm
tech.root: debugger
ms.date: 05/03/2018
keywords: ["IDebugClient5::TerminateCurrentProcess"]
ms.keywords: IDebugClient2 interface [Windows Debugging],TerminateCurrentProcess method, IDebugClient2::TerminateCurrentProcess, IDebugClient3 interface [Windows Debugging],TerminateCurrentProcess method, IDebugClient3::TerminateCurrentProcess, IDebugClient4 interface [Windows Debugging],TerminateCurrentProcess method, IDebugClient4::TerminateCurrentProcess, IDebugClient5 interface [Windows Debugging],TerminateCurrentProcess method, IDebugClient5.TerminateCurrentProcess, IDebugClient5::TerminateCurrentProcess, IDebugClient_7129a1e4-f1a5-4dff-a45c-bf759ae410cf.xml, TerminateCurrentProcess, TerminateCurrentProcess method [Windows Debugging], TerminateCurrentProcess method [Windows Debugging],IDebugClient2 interface, TerminateCurrentProcess method [Windows Debugging],IDebugClient3 interface, TerminateCurrentProcess method [Windows Debugging],IDebugClient4 interface, TerminateCurrentProcess method [Windows Debugging],IDebugClient5 interface, dbgeng/IDebugClient2::TerminateCurrentProcess, dbgeng/IDebugClient3::TerminateCurrentProcess, dbgeng/IDebugClient4::TerminateCurrentProcess, dbgeng/IDebugClient5::TerminateCurrentProcess, debugger.terminatecurrentprocess
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
 - IDebugClient5::TerminateCurrentProcess
 - dbgeng/IDebugClient5::TerminateCurrentProcess
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dbgeng.h
api_name:
 - IDebugClient5::TerminateCurrentProcess
---

# IDebugClient5::TerminateCurrentProcess


## -description

The <b>TerminateCurrentProcess</b> method attempts to terminate the current process.

## -parameters

## -returns

This method may also return error values.  See <a href="/windows-hardware/drivers/debugger/hresult-values">Return Values</a> for more details.

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

## -remarks

Only live user-modeprocesses are terminated by this method.  For other targets, the target is detached from the <a href="/windows-hardware/drivers/debugger/introduction">debugger engine</a> without terminating.

For more information about creating and attaching to live user-mode targets, see <a href="/windows-hardware/drivers/debugger/live-user-mode-targets">Live User-Mode Targets</a>.

## -see-also

<a href="/windows-hardware/drivers/debugger/-kill--kill-process-">.kill (Kill Process)</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugclient5-abandoncurrentprocess">AbandonCurrentProcess</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugclient5-attachprocess">AttachProcess</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugclient5-createprocessandattach2">CreateProcessAndAttach2</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugclient5-detachcurrentprocess">DetachCurrentProcess</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugclient2">IDebugClient2</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugclient3">IDebugClient3</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugclient4">IDebugClient4</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugclient5">IDebugClient5</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugclient5-terminateprocesses">TerminateProcesses</a>

