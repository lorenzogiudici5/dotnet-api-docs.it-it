### <a name="wpf-dispatchersynchronizationcontextcreatecopy-now-returns-a-new-copy-instead-of-the-current-instance"></a>WPF DispatcherSynchronizationContext.CreateCopy restituisce ora una nuova copia anziché l'istanza corrente

|   |   |
|---|---|
|Dettagli|In .NET Framework 4, <xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy> ha restituito un riferimento all'istanza corrente, principalmente come ottimizzazione delle prestazioni. In .NET Framework 4.5 restituisce una nuova istanza che rende possibile per la prima volta concludere che riferimenti uguali indicano che il thread in esecuzione è nel contesto di sincronizzazione corretto.  È improbabile che il codice che verifica l'identità di questi riferimenti sarà interessato, ma a causa della modifica, codice di cui viene chiamato <xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy> devono essere testati come parte della migrazione a .NET Framework 4.5 o versione successiva.|
|Suggerimento|Tenere presente che <xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy> restituirà ora un nuovo <xref:System.Threading.SynchronizationContext?displayProperty=name> oggetto. Nelle versioni precedenti, il codice che usa l'equivalenza dei riferimenti generati in questo modo non controlla in effetti se il contesto attivo è corretto, ma questa verifica viene eseguita se il codice viene compilato per .NET 4.5 o versione successiva.  Anche se è improbabile che si verifichino problemi, il test dei percorsi del codice interessati dovrebbe essere sufficiente per determinare se ciò costituisce un problema.|
|Ambito|Secondario|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy?displayProperty=nameWithType></li></ul>|

