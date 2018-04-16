### <a name="rsacng-now-correctly-loads-rsa-keys-of-non-standard-key-size"></a>RSACng ora correttamente carica chiavi RSA di dimensioni della chiave non standard

|   |   |
|---|---|
|Dettagli|Nelle versioni di .NET Framework precedenti alla 4.6.2, i clienti con dimensioni della chiave non standard per i certificati RSA sono in grado di accedere a tali chiavi tramite il <xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=name> e <xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPrivateKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=name> i metodi di estensione.  A <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> con il messaggio &quot;non è supportata la dimensione di chiave richiesta&quot; viene generata un'eccezione. In .NET Framework 4.6.2 è stato risolto il problema. Analogamente, <xref:System.Security.Cryptography.RSA.ImportParameters(System.Security.Cryptography.RSAParameters)> e <xref:System.Security.Cryptography.RSACng.ImportParameters(System.Security.Cryptography.RSAParameters)> ora funziona con dimensioni della chiave non standard senza generare <xref:System.Security.Cryptography.CryptographicException?displayProperty=name>s.|
|Suggerimento|Nel caso di eventuali eccezioni logica che si basa sul comportamento precedente in cui un <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> viene generata quando vengono utilizzate dimensioni della chiave non standard, provare a rimuovere la logica.|
|Ambito|Microsoft Edge|
|Versione|4.6.2|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.Security.Cryptography.RSA.ImportParameters(System.Security.Cryptography.RSAParameters)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.ImportParameters(System.Security.Cryptography.RSAParameters)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPrivateKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=nameWithType></li></ul>|
