### <a name="missing-target-framework-moniker-results-in-40-behavior"></a>Moniker del Framework di destinazione mancanti produce un comportamento 4.0

|   |   |
|---|---|
|Dettagli|Applicazioni senza un <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> applicato l'assembly a livello esegue automaticamente usando la semantica (quirks) di .NET Framework 4.0. Per assicurare la qualità elevata, è consigliabile che tutti i file binari in modo esplicito essere attribuito un <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> che indica la versione di .NET Framework sono state compilate con. Si noti che l'utilizzo di un moniker del framework di destinazione in un file di progetto farà MSBuild applicare automaticamente un <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>.|
|Suggerimento|Un <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> dovrebbe essere fornito mediante l'aggiunta dell'attributo direttamente all'assembly oppure specificando un framework di destinazione nel [file di progetto o tramite Visual Studio proiettare le proprietà GUI](http://blogs.msdn.com/b/visualstudio/archive/2010/05/19/visual-studio- managed-multi-targeting-part-1-concepts-target-framework-moniker-target-framework.aspx).|
|Ambito|Principale|
|Versione|4.5|
|Tipo|Runtime|

