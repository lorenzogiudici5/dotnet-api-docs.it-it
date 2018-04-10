### <a name="managed-browser-hosting-controls-from-the-net-framework-11-and-20-are-blocked"></a>I controlli di hosting di browser gestiti da .NET Framework 1.1 e 2.0 sono bloccati

|   |   |
|---|---|
|Dettagli|L'hosting di questi controlli è bloccato in Internet Explorer.|
|Suggerimento|Internet Explorer non riuscirà ad avviare un'applicazione che usa controlli di hosting di browser gestiti. Il comportamento precedente può essere ripristinato impostando il valore EnableIEHosting della sottochiave del Registro di sistema <code>HKLM/SOFTWARE/MICROSOFT/.NETFramework</code> al <code>1</code> x86 a sistemi e per processi a 32 bit su x64 sistemi e impostando il <code>EnableIEHosting</code> valore della sottochiave del Registro di sistema <code>HKLM/SOFTWARE/Wow6432Node/Microsoft/.NETFramework</code>a <code>1</code> per processi a 64 bit su x64 sistemi.|
|Ambito|Secondario|
|Versione|4.5|
|Tipo|Runtime|

