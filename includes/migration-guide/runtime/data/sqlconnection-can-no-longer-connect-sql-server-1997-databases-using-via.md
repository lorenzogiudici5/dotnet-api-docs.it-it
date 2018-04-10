### <a name="sqlconnection-can-no-longer-connect-to-sql-server-1997-or-databases-using-the-via-adapter"></a>SqlConnection non può più connettersi a SQL Server 1997 o database che utilizzano l'adapter VIA

|   |   |
|---|---|
|Dettagli|Le connessioni ai database di SQL Server mediante il [protocollo Adapter VIA (Virtual Interface)](https://technet.microsoft.com/library/ms191229%28v=sql.105%29.aspx) non sono più supportate. Il protocollo utilizzato per connettersi a un database di SQL Server è visibile nella stringa di connessione. Conterrà una connessione VIA via:&lt;servername&gt;. Se questa applicazione si connette a SQL tramite un protocollo diverso da VIA (tcp: o np: ad esempio), quindi non verrà rilevata nessuna modifica di rilievo. Inoltre, le connessioni a SQL Server 7 (1997) non sono più supportate.|
|Suggerimento|Il protocollo VIA è deprecato, pertanto un protocollo alternativo deve essere utilizzato per connettersi ai database SQL. Il protocollo più comune utilizzato è TCP/IP. È possibile trovare istruzioni per abilitare il protocollo TCP/IP [qui](https://msdn.microsoft.com/library/bb909712.aspx). Se il database è accessibile solo all'interno di una rete intranet, il protocollo condivisa pipe può fornire prestazioni migliori se la rete è lenta.|
|Ambito|Microsoft Edge|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String,System.Data.SqlClient.SqlCredential)?displayProperty=nameWithType></li></ul>|

