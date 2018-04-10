### <a name="building-an-entity-framework-edmx-with-visual-studio-2013-can-fail-with-error-msb4062-if-using-the-entitydeploysplit-or-entityclean-tasks"></a>La creazione di un edmx Entity Framework con Visual Studio 2013 può non riuscire con l'errore MSB4062 se tramite le attività EntityDeploySplit o EntityClean

|   |   |
|---|---|
|Dettagli|Strumenti di MSBuild 12.0 (inclusi in Visual Studio 2013) modificare i percorsi di file MSBuild, causando vecchi file di destinazioni di Entity Framework non è valido. Il risultato è che le attività <code>EntityDeploySplit</code> e <code>EntityClean</code> hanno esito negativo perché non sono in grado di trovare <code>Microsoft.Data.Entity.Build.Tasks.dll</code>. Si noti che questo tipo di interruzione a causa di una modifica di set di strumenti (MSBuild/Visual Studio), non a causa di una modifica di .NET Framework. Si verificherà solo quando si aggiornano gli strumenti di sviluppo, e non aggiornando semplicemente .NET Framework.|
|Suggerimento|File di destinazioni di Entity Framework sono fisse per funzionare con il nuovo MSBuild layout a partire da .NET Framework 4.6. L'aggiornamento a tale versione di .NET Framework consentirà di risolvere questo problema. In alternativa, è possibile usare [questa](http://stackoverflow.com/a/24249247/131944) soluzione alternativa per applicare una patch ai file di destinazioni direttamente.|
|Ambito|Principale|
|Versione|4.5.1|
|Tipo|Ridestinazione|

