### <a name="soapformatter-cannot-deserialize-hashtable-and-similar-ordered-collection-objects"></a>SoapFormatter non è possibile deserializzare Hashtable e simili ordinati oggetti della raccolta

|   |   |
|---|---|
|Dettagli|Il <xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> fa non garantisce che gli oggetti serializzati in una versione di .NET Framework verrà deserializzare correttamente in una versione diversa. In particolare, alcuni insiemi di ordinati (ad esempio <xref:System.Collections.Hashtable?displayProperty=name>) aggiunti i membri compresi tra 4.0 e 4.5 in modo che gli oggetti di questi tipi non è possibile deserializzare con .NET 4.0, se serializzate con .NET 4.5. Si noti che, se i dati serializzati vengono sia serializzati che deserializzati con la stessa versione di .NET Framework, non si verificherà alcun problema.|
|Suggerimento|<xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> serializzazione deve essere sostituita con <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> serializzazione o <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> adattabile alle modifiche di .NET Framework.|
|Ambito|Secondario|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object,System.Runtime.Remoting.Messaging.Header[])?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream,System.Runtime.Remoting.Messaging.HeaderHandler)?displayProperty=nameWithType></li></ul>|

