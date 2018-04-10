### <a name="wpf-layout-rounding-of-margins-has-changed"></a>Arrotondamento del layout WPF dei margini è stato modificato

|   |   |
|---|---|
|Dettagli|Il modo in cui i margini vengono arrotondati e i bordi e lo sfondo al loro interno vengono modificati. Come conseguenza di questo cambiamento:<ul><li>La larghezza o l'altezza degli elementi può aumentare o diminuire al massimo di un pixel.</li><li>La posizione di un oggetto può cambiare al massimo di un pixel.</li><li>Gli elementi centrati possono risultare decentrati in orizzontale o in verticale al massimo di un pixel.</li></ul>Per impostazione predefinita, questo nuovo layout è disponibile solo per app destinate a .NET Framework 4.6.|
|Suggerimento|Poiché questa modifica tende a eliminare il ritaglio del bordo destro o inferiore dei controlli WPF a DPI elevati, le app destinate alle versioni precedenti di .NET Framework ma vengono eseguiti in .NET Framework 4.6 possono adottare questo nuovo comportamento aggiungendo la riga seguente per il <code>&lt;runtime&gt;</code> sezione del file app. config: <code>&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.DoNotApplyLayoutRoundingToMarginsAndBorderThickness=false&quot; /&gt;</code>le app destinate a .NET Framework 4.6, ma i controlli WPF per eseguire il rendering usando l'algoritmo di layout precedente possono farlo aggiungendo la riga seguente al <code>&lt;runtime&gt;</code> sezione del file app. config: <code>&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.DoNotApplyLayoutRoundingToMarginsAndBorderThickness=true&quot; /&gt;</code>.|
|Ambito|Secondario|
|Versione|4.6|
|Tipo|Ridestinazione|

