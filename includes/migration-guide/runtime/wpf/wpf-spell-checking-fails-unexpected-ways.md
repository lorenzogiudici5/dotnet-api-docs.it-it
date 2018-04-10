### <a name="wpf-spell-checking-fails-in-unexpected-ways"></a>Controllo ortografico in WPF non riesce in modo imprevisto

|   |   |
|---|---|
|Dettagli|Ciò include un numero di problemi di controllo ortografico WPF:<ul><li>Controllo ortografico WPF genera talvolta <xref:System.Runtime.InteropServices.COMException?displayProperty=name></li><li>Controllo ortografico WPF non riesce con <xref:System.UnauthorizedAccessException> quando vengono avviate utilizzando 'Esegui come utente diverso'</li><li>Controllo ortografico WPF identifica in modo non corretto gli errori di ortografia in parole composte, ad esempio 'Hausnummer' in tedesco.</li></ul>|
|Suggerimento|Problema #1 - questo è stato risolto in .NET Framework 4.6.2 problema n. 2 - controllo ortografico WPF non è più supportata quando vengono avviate utilizzando 'Esegui come utente diverso'. A partire da .NET Framework 4.6.2, le applicazioni avviate in questo modo non si arresteranno in modo imprevisto: il controllo ortografico in alternativa, verrà disabilitato automaticamente. Problema #3 - questo è stato risolto in .NET Framework 4.6.2.|
|Ambito|Microsoft Edge|
|Versione|4.6.1|
|Tipo|Runtime|

