### <a name="wcf-msmqsecurehashalgorithm-default-value-is-now-sha256"></a>Valore predefinito MsmqSecureHashAlgorithm WCF è ora SHA256

|   |   |
|---|---|
|Dettagli|A partire da .NET Framework 4.7.1, il messaggio predefinito firma l'algoritmo di WCF per i messaggi Msmq è SHA256. In .NET Framework 4.7 e versioni precedenti, l'algoritmo di firma del messaggio predefinito è SHA1.|
|Suggerimento|Se si verificano problemi di compatibilità con questa modifica in .NET Framework 4.7.1 o versioni successive, è possibile rifiutare esplicitamente la modifica aggiungendo la riga seguente al <code>&lt;runtime&gt;</code>sezione del file app. config:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InMsmqEncryptionAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Ambito|Secondario|
|Versione|4.7.1|
|Tipo|Runtime|

