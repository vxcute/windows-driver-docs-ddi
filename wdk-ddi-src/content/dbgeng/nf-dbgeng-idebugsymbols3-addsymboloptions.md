---
UID: NF:dbgeng.IDebugSymbols3.AddSymbolOptions
title: IDebugSymbols3::AddSymbolOptions (dbgeng.h)
description: The AddSymbolOptions method turns on some of the engine's global symbol options. This method belongs to the IDebugSymbols3 interface.
old-location: debugger\addsymboloptions.htm
tech.root: debugger
ms.date: 05/03/2018
keywords: ["IDebugSymbols3::AddSymbolOptions"]
ms.keywords: AddSymbolOptions, AddSymbolOptions method [Windows Debugging], AddSymbolOptions method [Windows Debugging],IDebugSymbols interface, AddSymbolOptions method [Windows Debugging],IDebugSymbols2 interface, AddSymbolOptions method [Windows Debugging],IDebugSymbols3 interface, IDebugSymbols interface [Windows Debugging],AddSymbolOptions method, IDebugSymbols2 interface [Windows Debugging],AddSymbolOptions method, IDebugSymbols2::AddSymbolOptions, IDebugSymbols3 interface [Windows Debugging],AddSymbolOptions method, IDebugSymbols3.AddSymbolOptions, IDebugSymbols3::AddSymbolOptions, IDebugSymbols::AddSymbolOptions, IDebugSymbols_a7ffc5ae-fc9e-4298-a351-95871b8fd12e.xml, dbgeng/IDebugSymbols2::AddSymbolOptions, dbgeng/IDebugSymbols3::AddSymbolOptions, dbgeng/IDebugSymbols::AddSymbolOptions, debugger.addsymboloptions
req.header: dbgeng.h
req.include-header: Dbgeng.h, Dbghelp.h
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
 - IDebugSymbols3::AddSymbolOptions
 - dbgeng/IDebugSymbols3::AddSymbolOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dbgeng.h
api_name:
 - IDebugSymbols3::AddSymbolOptions
---

# IDebugSymbols3::AddSymbolOptions


## -description

The <b>AddSymbolOptions</b> method turns on some of the engine's global symbol options.

## -parameters

### -param Options 

[in]
Specifies the symbol options to turns on.  <i>Options</i> is a bit-set that will be ORed with the existing symbol options.  For a description of the bit flags, see <a href="/windows-hardware/drivers/debugger/symbol-options">Setting Symbol Options</a>.

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
 

This method may also return error values.  See <a href="/windows-hardware/drivers/debugger/hresult-values">Return Values</a> for more details.

## -remarks

After the symbol options have been changed, for each client the engine sends out notification to that client's <a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugeventcallbacks">IDebugEventCallbacks</a> by passing the DEBUG_CES_SYMBOL_OPTIONS flag to the <a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugeventcallbacks-changesymbolstate">IDebugEventCallbacks::ChangeSymbolState</a> method.

For more information about symbols, see <a href="/windows-hardware/drivers/debugger/symbols4">Symbols</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugsymbols3-getsymboloptions">GetSymbolOptions</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugsymbols">IDebugSymbols</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugsymbols2">IDebugSymbols2</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugsymbols3">IDebugSymbols3</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugsymbols3-removesymboloptions">RemoveSymbolOptions</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugsymbols3-setsymboloptions">SetSymbolOptions</a>

