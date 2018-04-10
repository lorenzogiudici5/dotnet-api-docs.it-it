### <a name="item-scrolling-a-flat-list-with-items-of-different-pixel-height"></a>Un elenco semplice con gli elementi dell'altezza di pixel diversa lo scorrimento elemento

|   |   |
|---|---|
|Dettagli|Quando un <xref:System.Windows.Controls.ItemsControl?displayProperty=name> Visualizza una raccolta mediante la virtualizzazione (<code>IsVirtualizing=true</code>) e articolo scorrimento (<code>ScrollUnit=Item</code>), e quando si scorre il controllo per visualizzare un elemento la cui altezza in pixel è diverso dal router adiacenti, il <xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name> scorre tutti elementi della raccolta. L'interfaccia utente non risponde durante questa iterazione. Se la raccolta è di grandi dimensioni, questo può essere percepito come un blocco. Si verifica l'iterazione in altre circostanze, anche nelle versioni precedenti di .net. Ad esempio, si verifica durante lo scorrimento pixel (<code>ScrollUnit=Pixel</code>) in presenza di un elemento con altezza in pixel diversa e durante lo scorrimento elemento dati gerarchici (ad esempio un <xref:System.Windows.Controls.TreeView?displayProperty=name> o un <xref:System.Windows.Controls.ItemsControl?displayProperty=name> con raggruppamento abilitato) in presenza di un elemento con un numero diverso di elementi discendenti più gli elementi adiacenti. Nel caso di altezza in pixel diverse e lo scorrimento elemento, l'iterazione è stata introdotta in .net 4.6.1 per correggere i bug nel layout di dati gerarchici.  Non è necessaria se i dati flat (alcuna gerarchia) e .net 4.6.2 questa non viene eseguita in questo caso.|
|Suggerimento|Se l'iterazione si verifica in .net 4.6.1 ma non nelle versioni precedenti, vale a dire, se il <xref:System.Windows.Controls.ItemsControl?displayProperty=name> è lo scorrimento di un elenco semplice elemento-elementi di pixel diversa altezza - non vi sono due rimedi:<ol><li>Installare .net 4.6.2.</li><li>Installare l'hotfix 1605 delle risorse Umane per .net 4.6.1.</li></ol>|
|Ambito|Secondario|
|Versione|4.6.1|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=nameWithType></li></ul>|

