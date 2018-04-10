### <a name="targetframeworkname-for-default-app-domain-no-longer-defaults-to-null-if-not-set"></a>TargetFrameworkName per dominio applicazione predefinito non è più sarà per impostazione predefinita null se non impostato

|   |   |
|---|---|
|Dettagli|Il <xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> era in precedenza null nel dominio applicazione predefinito, a meno che non è stata impostata in modo esplicito. A partire da 4.6, il <xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> proprietà per il dominio applicazione predefinito avrà valore predefinito è derivato da TargetFrameworkAttribute (se presente). Domini applicazione non predefinito continuerà a ereditare loro <xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> dal dominio applicazione predefinito (che non utilizzerà null nella versione 4.6) a meno che non sia sottoposto a override in modo esplicito.|
|Suggerimento|Il codice deve essere aggiornato in modo che non dipenda dal fatto che l'impostazione predefinita di <xref:System.AppDomainSetup.TargetFrameworkName> sia null. Se è necessario che questa proprietà continui a restituire null, è possibile impostarla in modo esplicito su tale valore.|
|Ambito|Microsoft Edge|
|Versione|4.6|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=nameWithType></li></ul>|

