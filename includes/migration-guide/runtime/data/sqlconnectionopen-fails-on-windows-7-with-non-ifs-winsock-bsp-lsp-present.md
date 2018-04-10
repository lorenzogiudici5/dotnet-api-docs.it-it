### <a name="sqlconnectionopen-fails-on-windows-7-with-non-ifs-winsock-bsp-or-lsp-present"></a>SqlConnection.Open non riesce in Windows 7 con LSP presente o non - IFS Winsock base Service Provider

|   |   |
|---|---|
|Dettagli|<xref:System.Data.SqlClient.SqlConnection.Open> e <xref:System.Data.SqlClient.SqlConnection.OpenAsync(System.Threading.CancellationToken)> esito negativo in .NET Framework 4.5, se in esecuzione in un computer Windows 7 con un LSP non IFS Winsock BSP sono presenti nel computer. Per determinare se è installato un non - IFS BSP o LSP, usare il <code>netsh WinSock Show Catalog</code> comando ed esaminare ogni <code>Winsock Catalog Provider Entry</code> elemento restituito. Se per il valore Service Flags è impostato il bit <code>0x20000</code>, il provider usa handle IFS e funzionerà correttamente. Se il bit <code>0x20000</code> non è impostato, si tratta di un LSP o BSP non-IFS.|
|Suggerimento|Questo bug è stato risolto in .NET Framework 4.5.2, pertanto può essere evitato eseguendo l'aggiornamento di .NET Framework. In alternativa, è possibile evitarlo rimuovendo qualsiasi provider LSP Winsock non-IFS installato.|
|Ambito|Secondario|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Data.SqlClient.SqlConnection.Open?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.OpenAsync(System.Threading.CancellationToken)?displayProperty=nameWithType></li></ul>|

