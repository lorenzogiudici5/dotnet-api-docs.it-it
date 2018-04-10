### <a name="appdomainsetupdynamicbase-is-no-longer-randomized-by-userandomizedstringhashalgorithm"></a>AppDomainSetup.DynamicBase non è casuale non è più da UseRandomizedStringHashAlgorithm

|   |   |
|---|---|
|Dettagli|Prima di .NET Framework 4.6, il valore di <xref:System.AppDomainSetup.DynamicBase> potrebbe essere casuale tra i domini applicazione o tra processi, se UseRandomizedStringHashAlgorithm è stato abilitato nel file di configurazione dell'app. A partire da .NET Framework 4.6, <xref:System.AppDomainSetup.DynamicBase> restituirà un risultato stabile tra istanze diverse di un'esecuzione di app e tra domini di applicazione diversi. Basi dinamiche saranno comunque diversi per diverse App; Questa modifica rimuove solo l'elemento denominazione casuale per le diverse istanze della stessa app.|
|Suggerimento|Tenere presente che l'abilitazione <code>UseRandomizedStringHashAlgorithm</code> non comporterà <xref:System.AppDomainSetup.DynamicBase> in corso casuale. Se è necessaria una base casuale, devono essere prodotti nel codice dell'app invece che tramite questa API.|
|Ambito|Microsoft Edge|
|Versione|4.6|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.AppDomainSetup.DynamicBase?displayProperty=nameWithType></li></ul>|

