### <a name="incorrect-code-generation-when-passing-and-comparing-uint16-values"></a>Generazione di codice non corretto quando il passaggio e confronto di valori UInt16.

|   |   |
|---|---|
|Dettagli|A causa di modifiche introdotte in 4.7 il Framework .NET, in alcuni casi il codice generato dal compilatore JIT in applicazioni in esecuzione su 4.7 il Framework .NET in modo non corretto Confronta due <code>T:System.UInt16</code> valori. Per altre informazioni, vedere [problema #11508: corretto codegen quando passaggio e confronto args ushort](https://github.com/dotnet/coreclr/issues/11508) su GitHub.com.|
|Suggerimento|Se si verificano problemi nel confronto di valori senza segno a 16 bit in 4.7 il Framework .NET, eseguire l'aggiornamento a .NET Framework 4.7.1.|
|Ambito|Microsoft Edge|
|Versione|4.7|
|Tipo|Runtime|

