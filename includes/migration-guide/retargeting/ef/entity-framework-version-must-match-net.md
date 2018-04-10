### <a name="entity-framework-version-must-match-the-net-framework-version"></a>Versione di Entity Framework deve corrispondere alla versione di .NET Framework

|   |   |
|---|---|
|Dettagli|La versione di entity framework deve essere trovata una corrispondenza con la versione di .NET framework. Entity Framework 5 è consigliato per .NET 4.5. Esistono alcuni problemi noti con Entity Framework 4.x in un progetto .NET 4.5 intorno <xref:System.ComponentModel.DataAnnotations>. In .NET 4.5, questi sono stati spostati in un assembly diverso, pertanto vi sono problemi di determinare quali annotazioni da utilizzare.|
|Suggerimento|Eseguire l'aggiornamento a Entity Framework 5 per .NET Framework 4.5|
|Ambito|Principale|
|Versione|4.5|
|Tipo|Ridestinazione|

