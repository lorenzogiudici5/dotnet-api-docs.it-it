### <a name="certificate-eku-oid-validation"></a>Convalida del certificato OID EKU

|   |   |
|---|---|
|Dettagli|A partire da .NET Framework 4.6, il <xref:System.Net.Security.SslStream> o <xref:System.Net.ServicePointManager> classi eseguono la convalida di utilizzo chiavi avanzato (EKU) oggetto identificatore (OID). Un'estensione utilizzo chiavi avanzato (EKU) è una raccolta di identificatori di oggetto (OID) che indica le applicazioni che usano la chiave. Convalida OID EKU utilizza callback certificato remoto per assicurarsi che il certificato remoto disponga gli identificatori di oggetto corretti per lo scopo previsto.|
|Suggerimento|Se questa modifica è indesiderata, è possibile disabilitare OID EKU convalida del certificato aggiungendo quanto segue passare il [ \<AppContextSwitchOverrides >](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) nel [ ` ](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) del file di configurazione App:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Net.DontCheckCertificateEKUs=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre> <blockquote> [!IMPORTANT] Questa impostazione è disponibile solo per la compatibilità. L'uso in caso contrario, è sconsigliato.</blockquote> |
|Ambito|Secondario|
|Versione|4.6|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.Net.Security.SslStream?displayProperty=nameWithType></li><li><xref:System.Net.ServicePointManager?displayProperty=nameWithType></li><li><xref:System.Net.Http.HttpClient?displayProperty=nameWithType></li><li><xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType></li><li><xref:System.Net.HttpWebRequest?displayProperty=nameWithType></li><li><xref:System.Net.FtpWebRequest?displayProperty=nameWithType></li></ul>|

