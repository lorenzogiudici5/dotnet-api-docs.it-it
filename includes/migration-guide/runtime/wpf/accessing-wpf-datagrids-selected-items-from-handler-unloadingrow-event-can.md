### <a name="accessing-a-wpf-datagrids-selected-items-from-a-handler-of-the-datagrids-unloadingrow-event-can-cause-a-nullreferenceexception"></a>L'accesso a elementi selezionati a un WPF DataGrid da un gestore dell'evento UnloadingRow del DataGrid può causare un'eccezione NullReferenceException

|   |   |
|---|---|
|Dettagli|A causa di un bug in .NET Framework 4.5, gestori eventi per <xref:System.Windows.Controls.DataGrid> gli eventi che comportano la rimozione di una riga possono causare un <xref:System.NullReferenceException?displayProperty=name> se accedono i <xref:System.Windows.Controls.DataGrid>del <xref:System.Windows.Controls.Primitives.Selector.SelectedItem?displayProperty=name> o <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> proprietà.|
|Suggerimento|Questo problema è stato risolto in .NET Framework 4.6 e potrebbe essere risolto eseguendo l'aggiornamento a tale versione di .NET Framework.|
|Ambito|Secondario|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Windows.Controls.DataGrid.UnloadingRow?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.UnloadingRowDetails?displayProperty=nameWithType></li></ul>|

