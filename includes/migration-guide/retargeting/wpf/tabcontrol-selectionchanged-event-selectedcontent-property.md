### <a name="tabcontrol-selectionchanged-event-and-selectedcontent-property"></a>Evento TabControl SelectionChanged e SelectedContent proprietà

|   |   |
|---|---|
|Dettagli|A partire da .NET Framework 4.7.1, una <xref:System.Windows.Controls.TabControl> aggiorna il valore della relativa <xref:System.Windows.Controls.TabControl.SelectedContent> proprietà prima che venga generato il <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> evento quando cambia la selezione. In .NET Framework 4.7 e nelle versioni precedenti, l'aggiornamento a SelectedContent si sono verificati dopo l'evento.|
|Suggerimento|Le app che usano .NET Framework 4.7.1 o versioni successive possono rifiutare esplicitamente questo modificare e usare il comportamento legacy aggiungendo il comando seguente per il <code>&lt;runtime&gt;</code> sezione del file di configurazione dell'applicazione:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Le app destinate a .NET Framework 4.7 o versioni precedenti ma sono in esecuzione su .NET Framework 4.7.1 o in un secondo momento possibile abilitare il nuovo comportamento aggiungendo la riga seguente al <code>&lt;runtime&gt;</code> sezione del file .configuration dell'applicazione:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Ambito|Secondario|
|Versione|4.7.1|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.Windows.Controls.TabControl.SelectedContent?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.Selector.SelectionChanged?displayProperty=nameWithType></li></ul>|

