### <a name="mef-catalogs-implement-ienumerable-and-therefore-can-no-longer-be-used-to-create-a-serializer"></a>I cataloghi MEF implementano IEnumerable e pertanto non è più utilizzabile per creare un serializzatore

|   |   |
|---|---|
|Dettagli|A partire da .NET Framework 4.5, i cataloghi MEF implementano IEnumerable e pertanto non è più utilizzabile per creare un serializzatore (<xref:System.Xml.Serialization.XmlSerializer?displayProperty=name> oggetto). Il tentativo di serializzare un catalogo MEF genera un'eccezione.|
|Suggerimento|Non è più possibile usare MEF per creare un serializzatore|
|Ambito|Principale|
|Versione|4.5|
|Tipo|Runtime|

