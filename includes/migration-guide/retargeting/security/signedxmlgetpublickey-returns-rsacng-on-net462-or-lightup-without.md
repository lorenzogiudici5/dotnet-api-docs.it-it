### <a name="signedxmlgetpublickey-returns-rsacng-on-net462-or-lightup-without-retargeting-change"></a>SignedXml.GetPublicKey restituisce RSACng net462 (o lightup) senza modifiche di reindirizzamento

|   |   |
|---|---|
|Dettagli|A partire da .NET Framework 4.6.2, il tipo concreto dell'oggetto restituito dal <xref:System.Security.Cryptography.Xml.SignedXml.GetPublicKey%2A?displayProperty=nameWithType> metodo modificato (senza una particolarità) da un'implementazione CryptoServiceProvider a un'implementazione Cng. Infatti, l'implementazione è stata modificata dall'utilizzo <code>certificate.PublicKey.Key</code> all'utilizzo interno <code>certificate.GetAnyPublicKey</code> cui inoltra al <xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey%2A?displayProperty=nameWithType>.|
|Suggerimento|A partire da App in esecuzione su .NET Framework 4.7.1, è possibile usare l'implementazione di CryptoServiceProvider utilizzata per impostazione predefinita in .NET Framework 4.6.1 e versioni precedenti aggiungendo la seguente configurazione passa al [runtime](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)sezione del file di configurazione dell'app:<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.SignedXmlUseLegacyCertificatePrivateKey=true&quot; /&gt;&#13;&#10;</code></pre>|
|Ambito|Microsoft Edge|
|Versione|4.6.2|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.Security.Cryptography.Xml.SignedXml.CheckSignatureReturningKey(System.Security.Cryptography.AsymmetricAlgorithm@)?displayProperty=nameWithType></li></ul>|

