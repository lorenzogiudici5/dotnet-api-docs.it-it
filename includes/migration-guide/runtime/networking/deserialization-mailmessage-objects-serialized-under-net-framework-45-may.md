### <a name="deserialization-of-mailmessage-objects-serialized-under-the-net-framework-45-may-fail"></a>La deserializzazione degli oggetti MailMessage serializzato in .NET Framework 4.5 potrebbe non riuscire

|   |   |
|---|---|
|Dettagli|A partire da .NET Framework 4.5, <xref:System.Web.Mail.MailMessage> oggetti possono includere caratteri non ASCII. In .NET Framework 4, sono supportati solo caratteri ASCII. <xref:System.Web.Mail.MailMessage> gli oggetti che contengono caratteri non ASCII e che vengono serializzati in .NET Framework 4.5 o versioni successive non possono essere deserializzati in .NET Framework 4.|
|Suggerimento|Verificare che il codice fornisce la gestione delle eccezioni durante la deserializzazione di un <xref:System.Web.Mail.MailMessage> oggetto.|
|Ambito|Secondario|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Web.Mail.MailMessage?displayProperty=nameWithType></li></ul>|

