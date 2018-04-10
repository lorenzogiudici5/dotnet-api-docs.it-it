### <a name="no-longer-able-to-set-enableviewstatemac-to-false"></a>Non è più in grado di impostare EnableViewStateMac su false

|   |   |
|---|---|
|Dettagli|ASP.NET non consente più agli sviluppatori di specificare <code>&lt;pages enableViewStateMac=&quot;false&quot;/&gt;</code> o <code>&lt;@Page EnableViewStateMac=&quot;false&quot; %&gt;</code>. L'algoritmo Message Authentication Code (MAC) dello stato di visualizzazione viene ora applicato per tutte le richieste con stato di visualizzazione incorporato. Solo le app che impostano in modo esplicito la proprietà EnableViewStateMac a <code>false</code> sono interessate.|
|Suggerimento|EnableViewStateMac devono essere considerati true, e gli eventuali errori risultanti MAC devono essere risolti (come spiegato in [questa Guida](https://support.microsoft.com/kb/2915218), che contiene le soluzioni più a seconda delle specifiche di ciò che sta causando errori MAC).|
|Ambito|Principale|
|Versione|4.5.2|
|Tipo|Runtime|

