### <a name="systemthreadingtaskstask-no-longer-throw-objectdisposedexception-after-object-is-disposed"></a>Tasks non generano più ObjectDisposedException dopo l'eliminazione dell'oggetto

|   |   |
|---|---|
|Dettagli|Ad eccezione di <xref:System.Threading.Tasks.Task.System%23IAsyncResult%23AsyncWaitHandle>, <xref:System.Threading.Tasks.Task?displayProperty=name> metodi non generano più un' <xref:System.ObjectDisposedException?displayProperty=name> eccezione dopo l'eliminazione dell'oggetto. Questa modifica supporta l'utilizzo di attività memorizzate nella cache. Ad esempio, un metodo può restituire un'attività memorizzata nella cache per rappresentare un'operazione già completata anziché allocare una nuova attività. Ciò non è possibile nelle versioni precedenti di .NET Framework, perché qualsiasi utente dell'attività può rimuoverla e renderla così inutilizzabile.|
|Suggerimento|Tenere presente che i metodi di attività potrebbero non generano più <xref:System.ObjectDisposedException?displayProperty=name> in casi in cui l'oggetto è stato eliminato. Se un'app è stato a seconda di sapere che è stata eliminata in un'attività di questa eccezione, devono essere aggiornato per controllare in modo esplicito lo stato dell'attività utilizzando <xref:System.Threading.Tasks.Task.Status>.|
|Ambito|Secondario|
|Versione|4.5|
|Tipo|Runtime|

