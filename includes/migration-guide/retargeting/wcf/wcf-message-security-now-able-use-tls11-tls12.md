### <a name="wcf-message-security-now-is-able-to-use-tls11-and-tls12"></a>Protezione del messaggio WCF è ora in grado di utilizzare TLS1.1 e TLS1.2

|   |   |
|---|---|
|Dettagli|A partire da 4.7 il Framework .NET, i clienti configurabili TLS1.1 o TLS1.2 in sicurezza dei messaggi WCF oltre a SSL3.0 e TLS1.0 tramite impostazioni di configurazione dell'applicazione.|
|Suggerimento|In 4.7 il Framework .NET, il supporto per TLS1.1 e TLS1.2 nella sicurezza dei messaggi WCF è disabilitato per impostazione predefinita. È possibile abilitarlo aggiungendo la riga seguente al <code>&lt;runtime&gt;</code> sezione del file app. config o Web. config:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableUsingServicePointManagerSecurityProtocols=false;Switch.System.Net.DontEnableSchUseStrongCrypto=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Ambito|Microsoft Edge|
|Versione|4.7|
|Tipo|Ridestinazione|

