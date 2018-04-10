### <a name="wf-serializes-expressionsliterallttgt-datetimes-differently-now-breaks-custom-xaml-parsers"></a>WF serializza Expressions.Literal&lt;T&gt; date e ore in modo diverso a questo punto (interrompe i parser XAML personalizzati)

|   |   |
|---|---|
|Dettagli|L'oggetto associato <xref:System.Windows.Markup.ValueSerializer> convertirà l'oggetto un <xref:System.DateTime?displayProperty=name> o <xref:System.DateTimeOffset?displayProperty=name> oggetto il cui secondo e <xref:System.DateTime.Millisecond?displayProperty=name> componenti sono diversi da zero e (per un <xref:System.DateTime?displayProperty=name> valore) cui <xref:System.DateTime.Kind> proprietà non è specificata all'elemento di proprietà sintassi anziché una stringa. Tale modifica consente di eseguire il round trip dei valori di <xref:System.DateTime?displayProperty=name> e <xref:System.DateTimeOffset?displayProperty=name>. I parser XAML personalizzati che presuppongono che il codice XAML di input si trovi nella sintassi degli attributi non funzioneranno correttamente.|
|Suggerimento|Tale modifica consente di eseguire il round trip dei valori di <xref:System.DateTime?displayProperty=name> e <xref:System.DateTimeOffset?displayProperty=name>. I parser XAML personalizzati che presuppongono che il codice XAML di input si trovi nella sintassi degli attributi non funzioneranno correttamente.|
|Ambito|Microsoft Edge|
|Versione|4.5|
|Tipo|Runtime|

