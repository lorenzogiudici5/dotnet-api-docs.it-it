### <a name="resizing-a-grid-can-hang"></a>Possibile blocco durante il ridimensionamento di una griglia

|   |   |
|---|---|
|Dettagli|Durante il layout di <code>T:System.Windows.Controls.Grid</code> può verificarsi un ciclo infinito nelle circostanze seguenti:<ul><li>Le definizioni di riga contengono due *-righe che dichiarano entrambe un valore MinHeight e MaxHeight.</li><li>Il contenuto delle *-righe non supera il valore MaxHeight corrispondente</li><li>L'altezza disponibile della griglia viene superata dal primo valore MinHeight (più qualsiasi altra riga automatica o fissa)</li><li>L'app è destinata a .Net 4.7 o acconsente esplicitamente all'algoritmo di allocazione della versione 4.7 impostando <code>Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=false</code></li></ul>Il ciclo si verifica anche nel caso in cui siano presenti più di due righe o nel caso analogo per le colonne. Il problema è stato risolto in .Net 4.7.1.|
|Suggerimento|Eseguire l'aggiornamento a .Net 4.7.1.  In alternativa, se non è necessario l'algoritmo di allocazione della versione 4.7 è possibile usare l'impostazione di configurazione seguente:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Ambito|Microsoft Edge|
|Versione|4.7|
|Tipo|Runtime|

