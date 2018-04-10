### <a name="changing-the-isenabled-property-of-the-parent-of-a-textblock-control-affects-any-child-controls"></a>Modifica della proprietà IsEnabled dell'elemento padre di un controllo TextBlock influisce su tutti i controlli figlio

|   |   |
|---|---|
|Dettagli|A partire da .NET Framework 4.6.2, modificare il <xref:System.Windows.UIElement.IsEnabled?displayProperty=name> proprietà dell'elemento padre di un <xref:System.Windows.Controls.TextBlock?displayProperty=name> controllo influisce su tutti i controlli figlio (ad esempio collegamenti ipertestuali e i pulsanti) del <xref:System.Windows.Controls.TextBlock?displayProperty=name> controllo. In .NET Framework 4.6.1 e versioni precedenti, i controlli contenuti in un <xref:System.Windows.Controls.TextBlock?displayProperty=name> non sempre riflette lo stato del <xref:System.Windows.UIElement.IsEnabled?displayProperty=name> proprietà del <xref:System.Windows.Controls.TextBlock?displayProperty=name> padre.|
|Suggerimento|Nessuno. Questa modifica è conforme al comportamento previsto per i controlli all'interno di un controllo <xref:System.Windows.Controls.TextBlock?displayProperty=name>.|
|Ambito|Secondario|
|Versione|4.6.2|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Windows.UIElement.IsEnabled?displayProperty=nameWithType></li></ul>|

