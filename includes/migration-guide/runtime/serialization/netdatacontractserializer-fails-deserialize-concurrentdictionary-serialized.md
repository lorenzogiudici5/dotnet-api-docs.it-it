### <a name="netdatacontractserializer-fails-to-deserialize-a-concurrentdictionary-serialized-with-a-different-net-version"></a>NetDataContractSerializer non riesce a deserializzare un oggetto ConcurrentDictionary serializzato con una versione diversa di .NET

|   |   |
|---|---|
|Dettagli|Per impostazione predefinita, il <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> può essere utilizzato solo se entrambe le estremità serializzazione e deserializzazione condividono gli stessi tipi CLR. Pertanto, non è garantito che un oggetto serializzato con una versione di .NET Framework può essere deserializzato da una versione diversa.<xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> è un tipo che è noto a non deserializzare correttamente se serializzato con .NET Framework 4.5 o versioni precedenti e la deserializzazione con .NET Framework 4.5.1 o versioni successive.|
|Suggerimento|Sono disponibili numerosi possibili soluzioni alternative per risolvere questo problema:<ul><li>Aggiornare il computer per l'utilizzo di .NET Framework 4.5.1, anche la serializzazione.</li><li>Uso <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> invece di <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> come ciò non è previsto esattamente gli stessi tipi CLR in sia estremità serializzazione e deserializzazione.</li><li>Uso <xref:System.Collections.Generic.Dictionary%602?displayProperty=name> invece di <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> poiché non presenta questo particolare 4.5 -&gt;4.5.1 break.</li></ul>|
|Ambito|Secondario|
|Versione|4.5.1|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Runtime.Serialization.NetDataContractSerializer.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li></ul>|

