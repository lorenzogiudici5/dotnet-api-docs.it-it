### <a name="wcf-pipeconnectiongethashalgorithm-now-uses-sha256"></a>WCF PipeConnection.GetHashAlgorithm ora utilizza SHA256

|   |   |
|---|---|
|Dettagli|A partire da .NET Framework 4.7.1, Windows Communication Foundation Usa un hash SHA256 per generare nomi casuali per le named pipe. In .NET Framework 4.7 e versioni precedenti, utilizzato un hash SHA1.|
|Suggerimento|Se verifichino problemi di compatibilità con questa modifica in .NET Framework 4.7.1 o in un secondo momento, è possibile rifiutare esplicitamente, aggiungendo la riga seguente al <code>&lt;runtime&gt;</code> sezione del file app. config:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InPipeConnectionGetHashAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Ambito|Secondario|
|Versione|4.7.1|
|Tipo|Runtime|

