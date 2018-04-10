### <a name="wpf-textbox-selected-text-appears-a-different-color-when-the-text-box-is-inactive"></a>Testo di casella di testo WPF selezionata viene visualizzato un colore diverso quando la casella di testo è inattiva

|   |   |
|---|---|
|Dettagli|In .NET 4.5, se un controllo casella di testo WPF è inattivo (non ha lo stato attivo), il testo selezionato nella casella verrà visualizzato con un colore diverso rispetto a quando il controllo è attivo.|
|Suggerimento|Comportamento precedente (.NET 4.0) può essere ripristinato impostando il <xref:System.Windows.FrameworkCompatibilityPreferences.AreInactiveSelectionHighlightBrushKeysSupported> proprietà <code>false</code>.|
|Ambito|Microsoft Edge|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|

