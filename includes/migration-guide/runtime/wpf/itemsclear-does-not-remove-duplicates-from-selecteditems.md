### <a name="itemsclear-does-not-remove-duplicates-from-selecteditems"></a>Clear non rimuove i duplicati dal SelectedItems

|   |   |
|---|---|
|Dettagli|Si supponga che un selettore (con abilitata la selezione multipla) è duplicati relativa <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> raccolta - appare più volte lo stesso elemento.  Rimozione di tali elementi dall'origine dati (ad esempio chiamando Clear) ha esito negativo per rimuoverli da <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>; solo la prima istanza viene rimossa. Inoltre, utilizzo successivo delle <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> (ad esempio SelectedItems.Clear()) possono verificarsi problemi, ad esempio <xref:System.ArgumentException?displayProperty=name>, in quanto <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> contiene elementi che non sono più nell'origine dati.|
|Suggerimento|Eseguire l'aggiornamento se possibile a .NET 4.6.2.|
|Ambito|Secondario|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=nameWithType></li></ul>|

