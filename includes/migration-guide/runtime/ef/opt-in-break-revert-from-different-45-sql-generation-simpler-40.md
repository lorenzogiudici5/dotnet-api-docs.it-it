### <a name="opt-in-break-to-revert-from-different-45-sql-generation-to-simpler-40-sql-generation"></a>Interruzione di consenso esplicito per ripristinare dalla diversa generazione SQL 4.5 più semplice generazione SQL 4.0

|   |   |
|---|---|
|Dettagli|Le query che producono istruzioni JOIN e contengono una chiamata a un'operazione di limitazione senza prima utilizzando OrderBy ora produrre codice SQL più semplice. Dopo l'aggiornamento a .NET Framework 4.5, queste query producevano codice SQL più complesso rispetto alle versioni precedenti.|
|Suggerimento|Questa funzionalità è disabilitata per impostazione predefinita. Se Entity Framework genera istruzioni JOIN aggiuntive che causano una riduzione delle prestazioni, è possibile abilitare questa funzionalità aggiungendo la voce seguente al <code>&lt;appSettings&gt;</code> sezione del file di configurazione (app. config):<pre><code class="language-xml">&lt;add key=&quot;EntityFramework_SimplifyLimitOperations&quot; value=&quot;true&quot; /&gt;&#13;&#10;</code></pre>|
|Ambito|Trasparente|
|Versione|4.5.2|
|Tipo|Runtime|

