### <a name="apps-published-with-clickonce-that-use-a-sha-256-code-signing-certificate-may-fail-on-windows-2003"></a>Le app pubblicate con ClickOnce che usano un certificato di firma del codice SHA-256 potrebbero non riuscire in Windows 2003

|   |   |
|---|---|
|Dettagli|Il file eseguibile è firmato con SHA256. In precedenza, veniva firmato con SHA1 indipendentemente dal fatto che il certificato di firma del codice fosse SHA-1 o SHA-256. Si applica a:<ul><li>Tutte le applicazioni compilate con Visual Studio 2012 o versioni successive.</li><li>Applicazioni compilate con Visual Studio 2010 o versioni precedenti su sistemi in cui è presente .NET Framework 4.5.</li></ul>Se inoltre è presente .NET Framework 4.5 o versione successiva, il manifesto ClickOnce viene firmato anche con SHA-256 per i certificati SHA-256 indipendentemente dalla versione di .NET Framework per cui è stato compilato.|
|Suggerimento|La modifica della firma l'eseguibile di ClickOnce interessa solo i sistemi Windows Server 2003; è necessario che siano installati 938397 KB. La modifica della firma del manifesto con SHA-256 anche quando un'app è destinata a .NET Framework 4.0 o versioni precedenti introduce una dipendenza di runtime in .NET Framework 4.5 o versione successiva.|
|Ambito|Microsoft Edge|
|Versione|4.5|
|Tipo|Ridestinazione|

