### <a name="applicationfiltermessage-no-longer-throws-for-re-entrant-implementations-of-imessagefilterprefiltermessage"></a>Application.FilterMessage non genera più per le implementazioni rientrante di IMessageFilter. PreFilterMessage

|   |   |
|---|---|
|Dettagli|Prima di .NET Framework 4.6.1, con una chiamata <xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)> con un <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)> quale chiamato <xref:System.Windows.Forms.Application.AddMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name> o <xref:System.Windows.Forms.Application.RemoveMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name> (durante la chiamata anche <xref:System.Windows.Forms.Application.DoEvents>) causerebbe un <xref:System.IndexOutOfRangeException?displayProperty=name>. A partire da applicazioni destinate a .NET Framework 4.6.1, questa eccezione non viene più generata e filtri rientranti come descritto in precedenza possono essere utilizzati.|
|Suggerimento|Tenere presente che <xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)> non è più genererà per il rientrante <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)> comportamento descritto in precedenza. Questo influisce solo sulle applicazioni destinate al 4.6.1.Apps di .NET Framework, destinato a .NET Framework 4.6.1 può rifiutare esplicitamente questa modifica (o le app possono optare destinazione Framework precedenti) utilizzando il [DontSupportReentrantFilterMessage](~/docs/framework/migration-guide/mitigation-custom-imessagefilter-prefiltermessage-implementations.md#mitigation) opzione di compatibilità.|
|Ambito|Microsoft Edge|
|Versione|4.6.1|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)?displayProperty=nameWithType></li></ul>|

