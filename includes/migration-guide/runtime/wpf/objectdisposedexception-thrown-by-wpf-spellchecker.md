### <a name="objectdisposedexception-thrown-by-wpf-spellchecker"></a>ObjectDisposedException generata dal controllo ortografico WPF

|   |   |
|---|---|
|Dettagli|Applicazioni WPF occasionalmente arrestarsi in modo anomalo durante l'arresto dell'applicazione con un <xref:System.ObjectDisposedException?displayProperty=name> generata dal controllo ortografico. Questo problema è risolto in .NET 4.7 WPF, in quanto la gestione dell'eccezione normalmente in modo da garantire che le applicazioni possono essere influenzate negativamente non è più. Si noti che le eccezioni first-chance occasionali continuerà a essere osservate nelle applicazioni eseguite con un debugger.|
|Suggerimento|Eseguire l'aggiornamento a .NET 4.7|
|Ambito|Microsoft Edge|
|Versione|4.6.1|
|Tipo|Runtime|

