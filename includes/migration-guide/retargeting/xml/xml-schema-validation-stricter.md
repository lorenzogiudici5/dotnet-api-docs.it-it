### <a name="xml-schema-validation-is-stricter"></a>Convalida XML schema è più restrittiva

|   |   |
|---|---|
|Dettagli|In .NET Framework 4.5, convalida di XML schema è più rigida. Se si usa xsd:anyURI per convalidare un URI, come un protocollo mailto, la convalida ha esito negativo se sono presenti spazi nell'URI. Nelle versioni precedenti di .NET Framework la convalida aveva esito positivo. La modifica influisce solo sulle applicazioni destinate a .NET Framework 4.5.|
|Suggerimento|Convalida di .NET Framework 4.0 più blando è necessaria, l'applicazione convalida può far riferimento versione 4.0 di .NET Framework. Quando si ridestinazione a .NET 4.5, tuttavia, revisione del codice deve essere eseguita per essere certi che gli URI non valido (spazi inclusi) non sono previsti i valori di attributo con il tipo di dati anyURI.|
|Ambito|Secondario|
|Versione|4.5|
|Tipo|Ridestinazione|

