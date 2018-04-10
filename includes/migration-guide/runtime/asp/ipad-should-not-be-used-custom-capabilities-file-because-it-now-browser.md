### <a name="ipad-should-not-be-used-in-custom-capabilities-file-because-it-is-now-a-browser-capability"></a>IPad non deve essere utilizzato nel file di funzionalità personalizzata perché è ora una funzionalità del browser

|   |   |
|---|---|
|Dettagli|A partire da .NET 4.5, iPad è un identificatore nel file di funzionalità del browser ASP.NET predefinito, pertanto non deve essere utilizzata in un file di funzionalità personalizzate|
|Suggerimento|Se sono necessarie funzionalità specifiche per iPad, è necessario modificare il comportamento iPad impostando funzionalità per i gateway predefiniti refID &quot;IPad&quot; anziché tramite la generazione di un nuovo &quot;IPad&quot; ID dall'agente utente corrispondenza.|
|Ambito|Microsoft Edge|
|Versione|4.5|
|Tipo|Runtime|

