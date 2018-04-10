### <a name="attempting-a-tcpip-connection-to-a-sql-server-database-that-resolves-to-localhost-fails"></a>Tentare una connessione TCP/IP a un database di SQL Server che si risolve in `localhost` ha esito negativo

|   |   |
|---|---|
|Dettagli|In .NET Framework 4.6 e 4.6.1, tentare una connessione TCP/IP a un database di SQL Server che si risolve in <code>localhost</code> ha esito negativo con l'errore &quot;si è verificato un errore specifico dell'istanza o relativo alla rete durante il tentativo di stabilire una connessione a SQL Server. Il server non è stato trovato o non è accessibile. Verificare che il nome dell'istanza sia corretto e che SQL Server sia configurato in modo da consentire connessioni remote. (provider: interfacce di rete SQL, errore: 26 - errore nell'individuazione Server / dell'istanza specificati)&quot;|
|Suggerimento|Questo problema sia stato indirizzato e ripristinato il comportamento precedente in .NET Framework 4.6.2. Per connettersi a un Server SQL di Microsoft Azure che si risolve in <code>localhost</code>, eseguire l'aggiornamento a .NET Framework 4.6.2.|
|Ambito|Secondario|
|Versione|4.6|
|Tipo|Runtime|

