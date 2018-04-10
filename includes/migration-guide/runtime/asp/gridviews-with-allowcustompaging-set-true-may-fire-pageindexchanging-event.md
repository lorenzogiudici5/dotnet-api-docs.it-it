### <a name="gridviews-with-allowcustompaging-set-to-true-may-fire-the-pageindexchanging-event-when-leaving-the-final-page-of-the-view"></a>GridView con AllowCustomPaging impostato su true potrebbe generare l'evento PageIndexChanging quando si esce da pagina finale della visualizzazione

|   |   |
|---|---|
|Dettagli|Fa sì che un bug in .NET Framework 4.5 <xref:System.Web.UI.WebControls.GridView.PageIndexChanging?displayProperty=name> a volte non vengono attivati per <xref:System.Web.UI.WebControls.GridView?displayProperty=name>s che sono abilitati <xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=name>.|
|Suggerimento|Questo problema è stato risolto in .NET Framework 4.6 e potrebbe essere risolto eseguendo l'aggiornamento a tale versione di .NET Framework. Come una soluzione alternativa, è possibile eseguire l'app operazioni un BindGrid esplicita su qualsiasi <code>Page_Load</code> che raggiungeva queste condizioni (la <xref:System.Web.UI.WebControls.GridView?displayProperty=name> è nella pagina e ultimo ultimo<xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name> è diverso da <xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name>). In alternativa, l'app può essere modificata per consentire di paging (anziché il paging personalizzato), come lo scenario non viene illustrato il problema.|
|Ambito|Secondario|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=nameWithType></li></ul>|

