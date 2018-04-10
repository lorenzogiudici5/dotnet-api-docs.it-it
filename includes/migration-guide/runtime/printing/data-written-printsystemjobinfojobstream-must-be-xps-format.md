### <a name="data-written-to-printsystemjobinfojobstream-must-be-in-xps-format"></a>I dati scritti in PrintSystemJobInfo.JobStream devono essere in formato XPS

|   |   |
|---|---|
|Dettagli|Il <xref:System.Printing.PrintSystemJobInfo.JobStream> proprietà espone il flusso di un processo di stampa. L'utente può inviare dati non elaborati ai componenti di stampa del sistema operativo sottostanti scrivendo in questo flusso. A partire da .NET Framework 4.5 in Windows 8 e versioni successive del sistema operativo Windows, i dati scritti in questo flusso devono essere in formato XPS come flusso del pacchetto.|
|Suggerimento|Per ottenere l'output del contenuto di stampa, è possibile eseguire una delle operazioni seguenti:<ul><li>Usare la classe <xref:System.Windows.Xps.XpsDocumentWriter> per ottenere l'output del contenuto di stampa. Questa è l'alternativa consigliata.</li><li>Verificare che i dati inviati nel flusso restituito dal <xref:System.Printing.PrintSystemJobInfo.JobStream> proprietà è in formato XPS come flusso del pacchetto.</li></ul>|
|Ambito|Secondario|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Printing.PrintSystemJobInfo.JobStream?displayProperty=nameWithType></li></ul>|

