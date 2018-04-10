### <a name="workflow-now-throws-original-exception-instead-of-nullreferenceexception-in-some-cases"></a>Flusso di lavoro genera ora l'eccezione originale anziché NullReferenceException in alcuni casi

|   |   |
|---|---|
|Dettagli|In .NET Framework 4.6.2 e versioni precedenti, quando il metodo Execute di un'attività flusso di lavoro genera un'eccezione con un <code>null</code> valore per il <xref:System.Exception.Message> proprietà, il runtime del flusso di lavoro System. Activities genera un <xref:System.NullReferenceException?displayProperty=name>, maschera la eccezione originale. In 4.7 il Framework .NET, viene generata l'eccezione mascherato in precedenza.|
|Suggerimento|Se il codice si basa sulla gestione di <xref:System.NullReferenceException?displayProperty=name>, modificarlo per intercettare le eccezioni che potrebbero essere generate da attività personalizzate.|
|Ambito|Secondario|
|Versione|4.7|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Activities.CodeActivity.Execute(System.Activities.CodeActivityContext)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity%601.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.WorkflowInvoker.Invoke?displayProperty=nameWithType></li></ul>|

