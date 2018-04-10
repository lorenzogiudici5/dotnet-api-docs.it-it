### <a name="wpf-windows-are-rendered-without-clipping-when-extending-outside-a-single-monitor"></a>Finestre WPF il rendering vengono eseguiti senza ritaglio quando si estende di fuori di un solo monitor

|   |   |
|---|---|
|Dettagli|In .NET Framework 4.6 esecuzione su Windows 8 e versioni successive, l'intera finestra viene eseguito il rendering senza ritaglio quando si estende di fuori di singolo schermo in uno scenario con più monitor. Ciò è diverso rispetto alle versioni precedenti di .NET Framework che verrebbe ritagliare finestre WPF che esteso oltre un singolo schermo.|
|Suggerimento|Questo comportamento (se ritagliare o non) può essere impostato in modo esplicito utilizzando il <code>&lt;EnableMultiMonitorDisplayClipping&gt;</code> elemento <code>&lt;appSettings&gt;</code> nel file di configurazione dell'applicazione oppure impostando la <code>EnableMultiMonitorDisplayClipping</code> proprietà all'avvio dell'app.|
|Ambito|Secondario|
|Versione|4.6|
|Tipo|Runtime|

