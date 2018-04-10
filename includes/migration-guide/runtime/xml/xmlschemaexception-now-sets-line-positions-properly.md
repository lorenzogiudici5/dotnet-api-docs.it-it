### <a name="xmlschemaexception-now-sets-line-positions-properly"></a>XmlSchemaException imposta ora le posizioni delle righe in modo corretto

|   |   |
|---|---|
|Dettagli|Se il <xref:System.Xml.Linq.LoadOptions.SetLineInfo> valore viene passato al metodo Load e si verifica un errore di convalida, il <xref:System.Xml.Schema.XmlSchemaException.LineNumber> e <xref:System.Xml.Schema.XmlSchemaException.LinePosition> proprietà contengono ora informazioni sulla riga.|
|Suggerimento|Codice di gestione delle eccezioni che si presuppone <xref:System.Xml.Schema.XmlSchemaException.LineNumber> e <xref:System.Xml.Schema.XmlSchemaException.LinePosition> non saranno set deve essere aggiornato poiché queste proprietà verranno ora impostate correttamente quando SetLineInfo viene utilizzato durante il caricamento di dati XML.|
|Ambito|Microsoft Edge|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Xml.Linq.LoadOptions.SetLineInfo?displayProperty=nameWithType></li></ul>|

