### <a name="signedxml-and-encryptedxml-breaking-changes"></a>SignedXml ed EncryptedXml modifiche di rilievo

|   |   |
|---|---|
|Dettagli|In .NET Framework 4.6.2, correzioni rapide della sicurezza <xref:System.Security.Cryptography.Xml.SignedXml?displayProperty=name> e <xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=name> causare comportamenti diversi in fase di esecuzione. Ad esempio,<ul><li>Se un documento dispone di più elementi con lo stesso <code>id</code> attributo e una firma è destinato a uno di questi elementi come la radice della firma, il documento verrà considerato non valido.</li><li>Documenti utilizzando gli algoritmi di trasformazione XPath non canonica nei riferimenti ora vengono considerati non validi.</li><li>Documenti utilizzando gli algoritmi di trasformazione XSLT non canoniche nei riferimenti sono ora si consideri non valido.</li><li>Qualsiasi programma che si avvalgono di firme di risorse esterne scollegata sarà possibile eseguire questa operazione.</li></ul>|
|Suggerimento|Gli sviluppatori potrebbe essere necessario verificare la sintassi delle <xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform> e <xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform>, nonché i tipi derivati da <xref:System.Security.Cryptography.Xml.Transform> dopo un ricevitore di documento non può essere in grado di elaborarlo.|
|Ambito|Secondario|
|Versione|4.6.2|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Security.Cryptography.Xml.Transform?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.XmlDsigXPathTransform?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform?displayProperty=nameWithType></li></ul>|

