### <a name="ef-no-longer-throws-for-queryviews-with-specific-characteristics"></a>Entity Framework non genera più per elementi Queryview con caratteristiche specifiche

|   |   |
|---|---|
|Dettagli|Entity Framework non genera più un <xref:System.StackOverflowException?displayProperty=name> eccezione quando un'app esegue una query che coinvolge un elemento QueryView con una 0..1 proprietà di navigazione che tenta di includere le entità correlate come parte della query. Ad esempio chiamando <code>.Include(e =&gt; e.RelatedNavProp)</code>.|
|Suggerimento|Questa modifica riguarda solo il codice che usa elementi Queryview con 1-0..1 relazioni durante l'esecuzione di query che chiamano. Includere. Migliora l'affidabilità e dovrebbe essere trasparente a quasi tutte le app. Se tuttavia questa modifica causa un comportamento imprevisto, è possibile disabilitarla aggiungendo la voce seguente alla sezione <code>&lt;appSettings&gt;</code> del file di configurazione dell'app:<pre><code class="language-xml">&lt;add key=&quot;EntityFramework_SimplifyUserSpecifiedViews&quot; value=&quot;false&quot; /&gt;&#13;&#10;</code></pre>|
|Ambito|Microsoft Edge|
|Versione|4.5.2|
|Tipo|Runtime|

