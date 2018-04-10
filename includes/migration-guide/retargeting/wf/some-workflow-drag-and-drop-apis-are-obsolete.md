### <a name="some-workflow-drag-and-drop-apis-are-obsolete"></a>Alcune API di trascinamento e rilascio del flusso di lavoro sono obsoleti

|   |   |
|---|---|
|Dettagli|Questa API di trascinamento e rilascio del flusso di lavoro è obsoleta e genererà avvisi del compilatore se l'app viene rigenerato con 4.5.|
|Suggerimento|Nuovo <xref:System.Activities.Presentation.DragDropHelper?displayProperty=name> necessario utilizzare le API che supportano le operazioni con più oggetti. In alternativa, è possibile eliminare gli avvisi di compilazione o evitarli usando un compilatore precedente. Le API sono ancora supportate.|
|Ambito|Secondario|
|Versione|4.5|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.Activities.Presentation.DragDropHelper.DoDragMove(System.Activities.Presentation.WorkflowViewElement,System.Windows.Point)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetCompositeView(System.Windows.DragEventArgs)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetDraggedModelItem(System.Windows.DragEventArgs)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetDroppedObject(System.Windows.DependencyObject,System.Windows.DragEventArgs,System.Activities.Presentation.EditingContext)?displayProperty=nameWithType></li></ul>|

