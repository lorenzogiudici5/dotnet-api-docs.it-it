### <a name="improved-accessibility-for-some-net-sdk-tools"></a>Migliorare l'accessibilità per alcuni strumenti di .NET SDK

|   |   |
|---|---|
|Dettagli|In .NET Framework SDK 4.7.1, gli strumenti svcconfigedit.exe e svctraceviewer.exe sono stati migliorati tramite la correzione di problemi di accesso facilitato di variabili. Molti di questi sono stati piccoli inconvenienti, ad esempio un nome non definito o alcuni modelli di automazione interfaccia utente non è in corso implementati correttamente. Anche se molti utenti non essere consapevoli di questi valori non corretti, i clienti che utilizzano Assistive Technology, ad esempio gli screen reader troverà questi strumenti SDK più accessibile. Queste correzioni certamente, modificare alcuni comportamenti precedenti, ad esempio ordine dello stato attivo della tastiera. Per ottenere tutte le correzioni per l'accessibilità in questi strumenti, è possibile quanto segue al file app. config:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Ambito|Microsoft Edge|
|Versione|4.7.1|
|Tipo|Ridestinazione|

