### <a name="incorrect-implementation-of-memberdescriptorequals"></a>Implementazione non corretta del MemberDescriptor.Equals

|   |   |
|---|---|
|Dettagli|Implementazione originale del &quot;è uguale a&quot; metodo è stato il confronto di due proprietà di stringa diversa rispetto agli oggetti in confronto: nome della categoria per la stringa di descrizione. Per risolvere il problema consiste nel confrontare &quot;categoria&quot; del primo oggetto da &quot;categoria&quot; del secondo e &quot;descrizione&quot; a &quot;descrizione&quot;. Valore di configurazione MemberDescriptorEqualsReturnsFalseIfEquivalent può essere impostato su true per rifiutare esplicitamente il nuovo comportamento se la destinazione 4.6.2 o su false per abilitare questa correzione se la versione del framework di destinazione si trova sotto 4.6.2.|
|Suggerimento|Se l'applicazione dipende da MemberDescriptor.Equals talvolta restituendo false quando descrittori sono equivalenti e di destinazione 4.6.2 versione di .NET Framework, vengono offerte diverse opzioni:<ol><li>Apportare modifiche al codice per confrontare &quot;categoria&quot; e &quot;descrizione&quot; campi manualmente oltre all'esecuzione del metodo Equals.</li><li>Un rifiuto da questa modifica aggiungendo il seguente valore per il file app. config:</li></ol><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Se l'applicazione è destinata a 4.6.1 o versione precedente di .NET Framework e si desidera che questa modifica abilitata, è possibile impostare l'opzione di compatibilità su false aggiungendo il seguente valore per il file app. config:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Ambito|Microsoft Edge|
|Versione|4.6.2|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.ComponentModel.MemberDescriptor.Equals(System.Object)?displayProperty=nameWithType></li></ul>|

