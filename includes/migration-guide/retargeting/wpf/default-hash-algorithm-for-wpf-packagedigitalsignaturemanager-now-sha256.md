### <a name="the-default-hash-algorithm-for-wpf-packagedigitalsignaturemanager-is-now-sha256"></a>L'algoritmo hash predefinito per WPF principali è ora SHA256

|   |   |
|---|---|
|Dettagli|Il <code>System.IO.Packaging.PackageDigitalSignatureManager</code> fornisce funzionalità per le firme digitali in relazione i pacchetti WPF.  In .NET Framework 4.7 e versioni precedenti, l'algoritmo predefinito (<xref:System.IO.Packaging.PackageDigitalSignatureManager.DefaultHashAlgorithm?displayProperty=nameWithType>) utilizzato per firmare le parti di un pacchetto è stato SHA1.  A causa di problemi di sicurezza recenti con SHA1, questa impostazione predefinita è stata cambiata in SHA256 a partire da .NET Framework 4.7.1.  Questa modifica interessa tutte firmare il pacchetto, inclusi documenti XPS.|
|Suggerimento|Uno sviluppatore che desidera utilizzare questa modifica durante la scelta di una versione di framework sotto .NET 4.7.1 o uno sviluppatore che richiede la funzionalità precedente durante destinato a .NET 4.7.1 o superiore possono imposta il flag di AppContext seguente in modo appropriato.  Il valore true comporterà SHA1 viene utilizzato come l'algoritmo predefinito; restituisce false SHA256.<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.UseSha1AsDefaultHashAlgorithmForDigitalSignatures=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Ambito|Microsoft Edge|
|Versione|4.7.1|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.IO.Packaging.PackageDigitalSignatureManager.DefaultHashAlgorithm?displayProperty=nameWithType></li></ul>|

