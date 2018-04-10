### <a name="scrolling-a-wpf-treeview-or-grouped-listbox-in-a-virtualizingstackpanel-can-cause-a-hang"></a>Lo scorrimento di un controllo TreeView di WPF o ListBox raggruppati in un VirtualizingStackPanel può causare il blocco

|   |   |
|---|---|
|Dettagli|In v4.5 .NET Framework, lo scorrimento WPF <xref:System.Windows.Controls.TreeView?displayProperty=name> in uno stack virtualizzato pannello può causare blocchi se sono presenti i margini nel riquadro di visualizzazione (tra gli elementi di <xref:System.Windows.Controls.TreeView?displayProperty=name>, ad esempio, o su un elemento ItemsPresenter). In alcuni casi, inoltre, elementi di dimensioni diverse nella visualizzazione possono causare instabilità anche se non sono presenti margini.|
|Suggerimento|È possibile evitare questo bug eseguendo l'aggiornamento a .NET Framework 4.5.1. In alternativa, i margini possono essere rimossi dalle raccolte di visualizzazione (come <xref:System.Windows.Controls.TreeView?displayProperty=name>s) all'interno dello stack virtualizzato pannelli se tutti gli elementi contenuti sono della stessa dimensione.|
|Ambito|Principale|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Windows.Controls.VirtualizingStackPanel.SetIsVirtualizing(System.Windows.DependencyObject,System.Boolean)?displayProperty=nameWithType></li></ul>|

