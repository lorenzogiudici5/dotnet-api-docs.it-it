### <a name="the-net-framework-46-does-not-use-a-45xx-version-when-registering-itself-in-the-registry"></a>.NET Framework 4.6 non utilizza una versione 4.5.x.x durante la registrazione nel Registro di sistema

|   |   |
|---|---|
|Dettagli|Come ci si aspetterebbe, imposta la chiave della versione nel Registro di sistema (in <code>HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\NET Framework Setup\NDP\v4\Full</code>) per .NET Framework 4.6 inizia con '4.6', non 4.5. Le app che dipendono da queste chiavi del Registro di sistema per conoscere le versioni di .NET Framework installate in un computer devono essere aggiornate per comprendere che 4.6 è una nuova versione possibili e uno che sia compatibile con 4.5.x precedente rilascia.|
|Suggerimento|App di aggiornamento di probe per .NET Framework 4.5 installate cercando 4.5 chiavi del Registro di sistema per accettare anche 4.6.|
|Ambito|Microsoft Edge|
|Versione|4.6|
|Tipo|Runtime|

