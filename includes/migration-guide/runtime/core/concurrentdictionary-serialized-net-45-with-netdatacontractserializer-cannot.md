### <a name="a-concurrentdictionary-serialized-in-net-45-with-netdatacontractserializer-cannot-be-deserialized-by-net-451-or-452"></a>Un oggetto ConcurrentDictionary serializzato in .NET 4.5 con NetDataContractSerializer non può essere deserializzato in .NET 4.5.1 o 4.5.2

|   |   |
|---|---|
|Dettagli|A causa di modifiche interne al tipo, <xref:System.Collections.Concurrent.ConcurrentDictionary%602> oggetti serializzati con .NET Framework 4.5 utilizzando il <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> non può essere deserializzato in .NET Framework 4.5.1 o in 4.5.2.Note di .NET Framework che lo spostamento in altri (di direzione la serializzazione con .NET Framework 4.5.x e la deserializzazione con .NET Framework 4.5) funziona. Allo stesso modo, tutta la serializzazione tra versioni diverse di 4.x funziona con il 4.6.Serializing di .NET Framework e la deserializzazione con un'unica versione di .NET Framework non è interessata.|
|Suggerimento|Se è necessario serializzare e deserializzare una <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> tra .NET Framework 4.5 e .NET Framework 4.5.1/4.5.2, come un serializzatore alternativo il <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> oppure <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> serializzatore deve essere usato invece del <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>. In alternativa, perché questo problema viene risolto in .NET Framework 4.6, potrebbe essere risolto eseguendo l'aggiornamento a tale versione di .NET Framework.|
|Ambito|Secondario|
|Versione|4.5.1|
|Tipo|Runtime|

