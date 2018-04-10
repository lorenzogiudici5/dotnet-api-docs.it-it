### <a name="wcf-binding-with-the-transportwithmessagecredential-security-mode"></a>Binding WCF con la modalità di sicurezza TransportWithMessageCredential

|   |   |
|---|---|
|Dettagli|A partire da .NET Framework 4.6.1, binding WCF che utilizza la modalità di sicurezza TransportWithMessageCredential può essere impostato per ricevere i messaggi con senza segno &quot;a&quot; intestazioni per le chiavi di sicurezza asimmetrico. Per impostazione predefinita, non firmato &quot;a&quot; intestazioni continueranno a essere rifiutato nelle .NET 4.6.1. Essi verranno accettate solo se un'applicazione opts in questa nuova modalità di operazione che utilizza l'opzione di configurazione Switch.System.ServiceModel.AllowUnsignedToHeader. Poiché si tratta di una funzionalità di consenso, che non dovrebbe influire sul comportamento delle App esistenti.|
|Suggerimento|Poiché è una funzionalità che prevede il consenso esplicito, non dovrebbe influire sul comportamento delle app esistenti. Per controllare se il nuovo comportamento viene utilizzato o meno, usare l'impostazione di configurazione seguente:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.AllowUnsignedToHeader=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Ambito|Trasparente|
|Versione|4.6.1|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.ServiceModel.BasicHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.BasicHttpsSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.WSFederationHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li></ul>|

