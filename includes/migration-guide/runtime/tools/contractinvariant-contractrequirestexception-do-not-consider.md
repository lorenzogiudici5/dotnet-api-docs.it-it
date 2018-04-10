### <a name="contractinvariant-or-contractrequirestexception-do-not-consider-stringisnullorempty-to-be-pure"></a>Contract.Invariant o Contract.Requires<TException> non prendono in considerazione IsNullOrEmpty come pure

|   |   |
|---|---|
|Dettagli|Per le app destinate a .NET Framework 4.6.1, se contratto invariante per <xref:System.Diagnostics.Contracts.Contract.Invariant%2A?displayProperty=nameWithType> o il contratto di precondizione per <xref:System.Diagnostics.Contracts.Contract.Requires%2A?displayProperty=nameWithType)> chiama il <xref:System.String.IsNullOrEmpty%2A?displayProperty=nameWithType> metodo, il rewriter Genera avviso CC1036 del compilatore: &quot;rilevato chiamata al metodo ' System.String.IsNullOrWhteSpace(System.String)' senza [Pure] nel metodo.&quot; Si tratta di un avviso anziché un errore del compilatore del compilatore.|
|Suggerimento|Questo comportamento è stato affrontato nel [problema GitHub n. 339](https://github.com/Microsoft/CodeContracts/issues/339). Per eliminare questo avviso, è possibile scaricare e compilare una versione aggiornata del codice sorgente per lo strumento di contratti di codice dal [GitHub](https://github.com/Microsoft/CodeContracts/blob/master/README.md). Le informazioni per il download sono disponibili in fondo alla pagina.|
|Ambito|Secondario|
|Versione|4.6.1|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Diagnostics.Contracts.Contract.Invariant(System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Contracts.Contract.Requires(System.Boolean)?displayProperty=nameWithType></li></ul>|

