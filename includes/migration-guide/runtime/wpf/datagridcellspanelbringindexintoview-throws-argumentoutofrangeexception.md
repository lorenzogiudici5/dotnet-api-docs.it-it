### <a name="datagridcellspanelbringindexintoview-throws-argumentoutofrangeexception"></a>DataGridCellsPanel.BringIndexIntoView genera ArgumentOutOfRangeException

|   |   |
|---|---|
|Dettagli|<xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)> funziona in modo asincrono quando è abilitata la virtualizzazione di colonna, ma la larghezza delle colonne non è ancora stati determinati.  Se le colonne vengono rimosse prima che si verifichi il lavoro asincrono, un <xref:System.ArgumentOutOfRangeException?displayProperty=name> possono verificarsi.|
|Suggerimento|Uno dei seguenti:<ol><li>Eseguire l'aggiornamento a .NET 4.7.</li><li>Installare la patch più recente per la manutenzione per .NET 4.6.2.</li><li>Evitare la rimozione di colonne finché la risposta asincrona a <xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)> è stata completata.</li></ol>|
|Ambito|Microsoft Edge|
|Versione|4.6.2|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object,System.Windows.Controls.DataGridColumn)?displayProperty=nameWithType></li></ul>|

