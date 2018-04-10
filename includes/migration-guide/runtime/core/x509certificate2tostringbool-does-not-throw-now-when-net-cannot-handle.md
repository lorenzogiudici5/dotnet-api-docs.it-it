### <a name="x509certificate2tostringbool-does-not-throw-now-when-net-cannot-handle-the-certificate"></a>X509Certificate2.ToString(bool) generano ora quando .NET non può gestire il certificato

|   |   |
|---|---|
|Dettagli|In precedenza, questo metodo genererebbe se <code>true</code> passato per il parametro verbose e si sono verificati i certificati installati che non sono stati supportati da .NET Framework. A questo punto, il metodo abbia esito positivo e restituirà una stringa valida che vengono omesse le parti inaccessibile del certificato.|
|Suggerimento|Qualsiasi codice in base <xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)> devono essere aggiornati in modo da prevedere che la stringa restituita può escludere alcuni dati del certificato (ad esempio la chiave pubblica, la chiave privata e le estensioni) in alcuni casi in cui l'API sarebbe precedentemente generata l'eccezione.|
|Ambito|Microsoft Edge|
|Versione|4.6|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)?displayProperty=nameWithType></li></ul>|

