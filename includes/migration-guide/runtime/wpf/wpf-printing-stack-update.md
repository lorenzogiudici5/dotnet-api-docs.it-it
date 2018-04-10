### <a name="wpf-printing-stack-update"></a>Aggiornamento dello Stack di stampa WPF

|   |   |
|---|---|
|Dettagli|Utilizzando le API di stampa WPF <xref:System.Printing.PrintQueue?displayProperty=name> ora definito come stampa documento pacchetto API finestra a favore dell'API di stampa XPS ora deprecato. La modifica è stata eseguita con i servizi in considerazione; gli utenti né gli sviluppatori dovrebbe essere tutte le modifiche nel comportamento o l'utilizzo delle API. Il nuovo stack di stampa è abilitato per impostazione predefinita durante l'esecuzione in Windows 10 creatori di aggiornamento. Lo stack di stampa precedente ancora continueranno a funzionare solo come prima nelle versioni precedenti di Windows.|
|Suggerimento|Per usare lo stack precedente in Windows 10 creatori di aggiornamento, impostare il <code>UseXpsOMPrinting</code> valore REG_DWORD il <code>HKEY_CURRENT_USER\Software\Microsoft\.NETFramework\Windows Presentation Foundation\Printing</code> chiave del Registro di sistema per <code>1</code>.|
|Ambito|Microsoft Edge|
|Versione|4.7|
|Tipo|Runtime|

