### <a name="intermittently-unable-to-scroll-to-bottom-item-in-itemscontrols-like-listbox-and-datagrid-when-using-custom-datatemplates"></a>In modo intermittente non è possibile scorrere fino all'elemento inferiore ItemsControls (ad esempio, casella di riepilogo e DataGrid) quando si utilizza DataTemplate personalizzato

|   |   |
|---|---|
|Dettagli|In alcuni casi, un bug in .NET Framework 4.5 causa ItemsControls (ad esempio <xref:System.Windows.Controls.ListBox?displayProperty=name>, <xref:System.Windows.Controls.ComboBox?displayProperty=name>, <xref:System.Windows.Controls.DataGrid?displayProperty=name>e così via) non scorrere al relativo elemento inferiore quando si utilizza DataTemplate personalizzato. Lo scorrimento funzionerà se si esegue un secondo tentativo dopo uno scorrimento verso l'alto.|
|Suggerimento|Questo problema è stato corretto in .NET Framework 4.5.2 e può essere risolto eseguendo l'aggiornamento a tale versione di .NET Framework o a una versione successiva. In alternativa, gli utenti possono trascinare le barre di scorrimento fino agli elementi finali di queste raccolte, ma potrebbe essere necessario provare due volte per completare l'operazione correttamente.|
|Ambito|Secondario|
|Versione|4.5|
|Tipo|Runtime|

