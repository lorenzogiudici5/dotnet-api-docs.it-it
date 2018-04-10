### <a name="sqlbulkcopy-uses-destination-column-encoding-for-strings"></a>SqlBulkCopy utilizza la codifica di colonna di destinazione per le stringhe

|   |   |
|---|---|
|Dettagli|Nell'inserire i dati in una colonna, <xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name> usa la codifica della colonna di destinazione anziché quella predefinita per i tipi <code>VARCHAR</code> e <code>CHAR</code>. Questa modifica elimina la possibilità di danneggiamento dei dati causata dall'uso della codifica predefinita quando questa non viene usata dalla colonna di destinazione. In rari casi, un'applicazione esistente può generare un'eccezione SqlException se la modifica nella codifica produce dati troppo grandi per rientrare nella colonna di destinazione.|
|Suggerimento|Prevedere che <xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name> non danneggerà non è più dati a causa di differenze nella codifica. Se le stringhe in prossimità del limite di dimensioni della colonna di destinazione vengono copiate, potrebbe essere necessario codificare di pre-copiare i dati (per verificare che i dati rientrerà nella colonna di destinazione) o catch <xref:System.Data.SqlClient.SqlException?displayProperty=name>s.|
|Ambito|Microsoft Edge|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlBulkCopy.%23ctor(System.Data.SqlClient.SqlConnection)?displayProperty=nameWithType></li></ul>|

