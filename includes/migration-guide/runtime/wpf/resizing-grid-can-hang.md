### <a name="resizing-a-grid-can-hang"></a>Ridimensionamento di una griglia può bloccarsi

|   |   |
|---|---|
|Dettagli|Un ciclo infinito può verificarsi durante il layout di un <code>T:System.Windows.Controls.Grid</code> nelle circostanze seguenti:<ul><li>Le definizioni di righe contengono due *-righe, entrambi dichiarando un MinHeight e un MaxHeight.</li><li>Contenuto del *-righe non supera MaxHeight corrispondente</li><li>Altezza disponibile della griglia viene superato il primo MinHeight (più qualsiasi altro fissa o Auto righe)</li><li>L'app destinata a .net 4.7 o acconsente all'algoritmo di 4,7 allocazione impostando <code>Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=false</code></li></ul>Il ciclo verrà eseguite anche con più di due righe, o nel caso analogo per le colonne. Il problema viene risolto in .net 4.7.1.|
|Suggerimento|Eseguire l'aggiornamento a .net 4.7.1.  In alternativa, se non è necessario l'algoritmo di 4,7 allocazione è possibile utilizzare l'impostazione di configurazione seguente:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Ambito|Microsoft Edge|
|Versione|4.7|
|Tipo|Runtime|

