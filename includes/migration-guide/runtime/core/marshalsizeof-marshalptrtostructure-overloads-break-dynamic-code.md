### <a name="marshalsizeof-and-marshalptrtostructure-overloads-break-dynamic-code"></a>Marshal. sizeof e overload Marshal. PtrToStructure Interrompi dinamica del codice

|   |   |
|---|---|
|Dettagli|A partire da .NET Framework 4.5.1, associazione dinamica di ai metodi <xref:System.Runtime.InteropServices.Marshal.SizeOf%60%601>, <xref:System.Runtime.InteropServices.Marshal.SizeOf%60%601(%60%600)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure(System.IntPtr,System.Object)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure(System.IntPtr,System.Type)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure%60%601(System.IntPtr)>, o <xref:System.Runtime.InteropServices.Marshal.PtrToStructure%60%601(System.IntPtr,%60%600)>, (tramite Windows PowerShell, IronPython o il linguaggio c# parola chiave dinamica, ad esempio) può comportare <code>MethodInvocationExceptions</code> perché sono stati aggiunti nuovi overload di questi metodi che potrebbe essere ambigua per i motori di script.|
|Suggerimento|Aggiornare gli script per indicare chiaramente quale overload deve essere usato. Questa operazione può essere eseguita in genere tramite il cast esplicito dei parametri di tipo dei metodi su <xref:System.Type>. Vedere [questo collegamento](https://support.microsoft.com/kb/2909958/) per altri dettagli ed esempi per risolvere il problema.|
|Ambito|Secondario|
|Versione|4.5.1|
|Tipo|Runtime|

