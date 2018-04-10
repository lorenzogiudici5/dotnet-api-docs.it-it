### <a name="htmltextwriter-does-not-render-br-element-correctly"></a>Non esegue il rendering HtmlTextWriter `<br/>` elemento correttamente

|   |   |
|---|---|
|Dettagli|A partire da .NET Framework 4.6, la chiamata di <xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)> e <xref:System.Web.UI.HtmlTextWriter.RenderEndTag> con un elemento <code>&lt;BR /&gt;</code> inserirà correttamente solo un <code>&lt;BR /&gt;</code> (invece di due)|
|Suggerimento|Se un'app dipende dal tag <code>&lt;BR /&gt;</code> aggiuntivo, il metodo <xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)> deve essere chiamato una seconda volta. Si noti che questa modifica del comportamento influisce solo sulle App destinate a .NET Framework 4.6 o versione successivo, in modo che un'altra opzione destinati a una versione precedente di .NET Framework per ottenere il comportamento precedente.|
|Ambito|Microsoft Edge|
|Versione|4.6|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)?displayProperty=nameWithType></li><li><xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.Web.UI.HtmlTextWriterTag)?displayProperty=nameWithType></li></ul>|

