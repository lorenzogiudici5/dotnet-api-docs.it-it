### <a name="il-ret-not-allowed-in-a-try-region"></a>Linguaggio intermedio ret non consentita in un'area try

|   |   |
|---|---|
|Dettagli|A differenza del compilatore just-in-time di JIT64, RyuJIT (utilizzato in .NET 4.6) non consente un livello di integrità ret istruzione in un'area di riprovare. Restituzione da un'area try non è consentita dalla specifica ECMA-335 e nessun compilatore gestito noto genera tale. Tuttavia, il compilatore JIT64 eseguirà tale livello di integrità se viene generato tramite reflection emit.|
|Suggerimento|Un'app durante la generazione di linguaggio intermedio che include un codice operativo ret in un'area try, l'app potrebbero avere come destinazione .NET 4.5 per usare il compilatore JIT precedente ed evitare l'interruzione. In alternativa, il linguaggio intermedio generato può essere aggiornato per restituire dopo l'area di riprovare.|
|Ambito|Microsoft Edge|
|Versione|4.6|
|Tipo|Ridestinazione|

