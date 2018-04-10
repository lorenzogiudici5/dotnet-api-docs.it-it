### <a name="flowdocument-may-show-an-extra-line-of-text"></a>FlowDocument risultino una riga supplementare di testo

|   |   |
|---|---|
|Dettagli|In alcuni casi, un <xref:System.Windows.Documents.FlowDocument> elemento verrà visualizzato un'ulteriore riga di testo quando in esecuzione in .NET Framework 4.5 rispetto al modo in cui visualizzato durante l'esecuzione in .NET Framework 4.0. Esistono casi noti della modifica che causa il testo da visualizzare in modo inadeguato o illegibly, ma potrebbe impedire che in precedenza è stato omesso dal testo da visualizzare un <xref:System.Windows.Documents.FlowDocument>della visualizzazione.|
|Suggerimento|In alcuni casi, riducendo la visualizzazione proprietà dell'elemento PageHeight da una possibile ripristinare il precedente numero di righe visualizzate.|
|Ambito|Microsoft Edge|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Windows.Documents.FlowDocument.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Documents.FlowDocument.%23ctor(System.Windows.Documents.Block)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentReader.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentPageViewer.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.DocumentPageView.%23ctor?displayProperty=nameWithType></li></ul>|

