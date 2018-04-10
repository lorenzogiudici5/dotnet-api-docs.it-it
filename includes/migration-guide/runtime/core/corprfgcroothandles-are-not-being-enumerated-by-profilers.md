### <a name="corprfgcroothandles-are-not-being-enumerated-by-profilers"></a>COR_PRF_GC_ROOT_HANDLEs non vengono enumerate profiler

|   |   |
|---|---|
|Dettagli|Nel v4.5.1 di .NET Framework, l'API di profilatura <code>RootReferences2()</code> erroneamente mai la restituzione <code>COR_PRF_GC_ROOT_HANDLE</code> (cioè vengono restituiti come <code>COR_PRF_GC_ROOT_OTHER</code> invece). Questo problema è risolto a partire da .NET Framework 4.6.|
|Suggerimento|Questo problema è stato risolto in .NET Framework 4.6 e potrebbe essere risolto eseguendo l'aggiornamento a tale versione di .NET Framework.|
|Ambito|Secondario|
|Versione|4.5.1|
|Tipo|Runtime|

