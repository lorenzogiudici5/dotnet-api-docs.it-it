### <a name="workflowdesignerload-doesnt-remove-symbol-property"></a>WorkflowDesigner.Load non lo rimuove proprietà simbolo

|   |   |
|---|---|
|Dettagli|Quando la destinazione di .NET Framework 4.5 nella finestra di progettazione del flusso di lavoro e il caricamento di un flusso di lavoro 3.5 rieseguito nell'host con il <xref:System.Activities.Presentation.WorkflowDesigner.Load> metodo, un <xref:System.Xaml.XamlDuplicateMemberException?displayProperty=name> viene generata durante il salvataggio del flusso di lavoro.|
|Suggerimento|Questo bug manifesti solo quando la destinazione è .NET Framework 4.5 nella finestra di progettazione del flusso di lavoro, in modo che possa essere elaborata intorno impostando il <code>WorkflowDesigner.Context.Services.GetService&lt;DesignerConfigurationService&gt;().TargetFrameworkName</code> per il Framework.Alternatively .NET 4.0, il problema può essere evitato utilizzando il <xref:System.Activities.Presentation.WorkflowDesigner.Load(System.String)> metodo per caricare il flusso di lavoro, invece di <xref:System.Activities.Presentation.WorkflowDesigner.Load>.|
|Ambito|Principale|
|Versione|4.5|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.Activities.Presentation.WorkflowDesigner.Load?displayProperty=nameWithType></li></ul>|

