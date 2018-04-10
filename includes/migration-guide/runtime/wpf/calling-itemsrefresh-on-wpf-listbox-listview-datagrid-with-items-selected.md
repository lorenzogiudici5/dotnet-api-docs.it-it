### <a name="calling-itemsrefresh-on-a-wpf-listbox-listview-or-datagrid-with-items-selected-can-cause-duplicate-items-to-appear-in-the-element"></a>Items.Refresh chiamata su un controllo ListBox di WPF, ListView o DataGrid con gli elementi selezionati possono essere causa elementi duplicati da visualizzare nell'elemento

|   |   |
|---|---|
|Dettagli|In .NET Framework 4.5, chiamata ListBox.Items.Refresh dal codice, mentre gli elementi selezionati in un <xref:System.Windows.Controls.ListBox?displayProperty=name> può causare gli elementi selezionati essere duplicati nell'elenco. Si verifica un problema analogo <xref:System.Windows.Controls.ListView?displayProperty=name> e <xref:System.Windows.Controls.DataGrid?displayProperty=name>. Questo problema è risolto in .NET Framework 4.6.|
|Suggerimento|Questo problema potrebbe essere ha lavorato intorno a livello di codice se si deseleziona elementi prima <xref:System.Windows.Data.CollectionView.Refresh?displayProperty=name> viene chiamato e quindi nuovamente selezionandoli dopo la chiamata è stata completata. In alternativa, questo problema è stato corretto in .NET Framework 4.6 e può essere risolto eseguendo l'aggiornamento a tale versione di .NET Framework.|
|Ambito|Secondario|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Windows.Data.CollectionView.Refresh?displayProperty=nameWithType></li></ul>|

