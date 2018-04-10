### <a name="rsacngverifyhash-now-returns-false-for-any-verification-failure"></a>RSACng.VerifyHash ora restituisce False per qualsiasi errore di verifica

|   |   |
|---|---|
|Dettagli|A partire da .NET Framework 4.6.2, questo metodo restituisce <strong>False</strong> se non è formattata correttamente la firma stessa. Ora restituisce false per qualsiasi errore di verifica. In .NET Framework 4.6 e 4.6.1, il metodo genera un <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> se non è formattata correttamente la firma stessa.|
|Suggerimento|Qualsiasi codice la cui esecuzione dipende dalla gestione di <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> deve essere eseguita in alternativa, se la convalida non riesce e il metodo restituisce <strong>False</strong>.|
|Ambito|Secondario|
|Versione|4.6.2|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Security.Cryptography.RSACng.VerifyHash(System.Byte[],System.Byte[],System.Security.Cryptography.HashAlgorithmName,System.Security.Cryptography.RSASignaturePadding)?displayProperty=nameWithType></li></ul>|

