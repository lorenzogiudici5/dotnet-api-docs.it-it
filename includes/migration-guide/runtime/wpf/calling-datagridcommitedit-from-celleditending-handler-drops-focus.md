### <a name="calling-datagridcommitedit-from-a-celleditending-handler-drops-focus"></a>Chiamata di DataGrid.CommitEdit da un gestore CellEditEnding Elimina lo stato attivo

|   |   |
|---|---|
|Dettagli|La chiamata <xref:System.Windows.Controls.DataGrid.CommitEdit> da uno del <xref:System.Windows.Controls.DataGrid?displayProperty=name>del <xref:System.Windows.Controls.DataGrid.CellEditEnding?displayProperty=name> fa sì che i gestori di eventi il <xref:System.Windows.Controls.DataGrid?displayProperty=name> per perdere lo stato attivo.|
|Suggerimento|Questo bug è stato risolto in .NET Framework 4.5.2, pertanto può essere evitato eseguendo l'aggiornamento di .NET Framework. In alternativa, può essere evitato selezionando in modo esplicito nuovamente il <xref:System.Windows.Controls.DataGrid?displayProperty=name> dopo la chiamata <xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=name>.|
|Ambito|Microsoft Edge|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.CommitEdit(System.Windows.Controls.DataGridEditingUnit,System.Boolean)?displayProperty=nameWithType></li></ul>|

