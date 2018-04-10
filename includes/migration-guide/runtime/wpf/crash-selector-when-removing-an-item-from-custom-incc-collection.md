### <a name="crash-in-selector-when-removing-an-item-from-a-custom-incc-collection"></a>Quando si rimuove un elemento da una raccolta personalizzata INCC di arresto anomalo nel selettore

|   |   |
|---|---|
|Dettagli|Un <code>T:System.InvalidOperationException</code> può verificarsi nel seguente scenario:<ul><li>ItemsSource per un <code>T:System.Windows.Controls.Primitives.Selector</code> è una raccolta con un'implementazione personalizzata di <code>T:System.Collections.Specialized.INotifyCollectionChanged</code>.</li><li>L'elemento selezionato viene rimosso dalla raccolta.</li><li>Il <code>T:System.Collections.Specialized.NotifyCollectionChangedEventArgs</code> ha <code>P:System.Collections.Specialized.NotifyCollectionChangedEventArgs.OldStartingIndex</code> = -1 (che indica una posizione sconosciuta).</li></ul>Stack di chiamate dell'eccezione in cui inizia System.Windows.Threading.Dispatcher.VerifyAccess() in System.Windows.DependencyObject.GetValue (dp DependencyProperty) in System.Windows.Controls.Primitives.Selector.GetIsSelected (DependencyObject elemento) questa eccezione può verificarsi in .net 4.5 se l'applicazione ha più di un thread del Dispatcher. In .net 4.7 l'eccezione può verificarsi anche in applicazioni con un singolo thread del Dispatcher. Il problema viene risolto in .net 4.7.1.|
|Suggerimento|Eseguire l'aggiornamento a .net 4.7.1.|
|Ambito|Secondario|
|Versione|4.7|
|Tipo|Runtime|

