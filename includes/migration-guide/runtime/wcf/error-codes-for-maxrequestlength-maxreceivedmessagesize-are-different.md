### <a name="error-codes-for-maxrequestlength-or-maxreceivedmessagesize-are-different"></a>Codici di errore per maxRequestLength o maxReceivedMessageSize sono diversi

|   |   |
|---|---|
|Dettagli|I messaggi in WCF servizi web ospitati in Internet Information Services (IIS) o nel Server di sviluppo ASP.NET che superano maxRequestLength (in ASP.NET) o maxReceivedMessageSize (in WCF) dispone di diversi errore codice di stato codeThe HTTP è stato modificato da 400 (richiesta non valida ) a 413 (entità della richiesta troppo grande) e i messaggi che superano il maxRequestLength o l'impostazione di maxReceivedMessageSize generano un <xref:System.ServiceModel.ProtocolException?displayProperty=name> (eccezione). Sono inclusi i casi in cui viene trasmessa la modalità di trasferimento.|
|Suggerimento|Questa modifica semplifica il debug nei casi in cui la lunghezza del messaggio supera i limiti consentiti da ASP.NET o WCF. È necessario modificare qualsiasi codice che esegue l'elaborazione in base a un codice di stato HTTP 400.|
|Ambito|Microsoft Edge|
|Versione|4.5|
|Tipo|Runtime|

