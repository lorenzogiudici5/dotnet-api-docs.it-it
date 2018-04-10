### <a name="unicode-standard-version-80-categories-now-supported"></a>Categorie di Unicode standard versione 8.0 ora supportate

|   |   |
|---|---|
|Dettagli|In .NET Framework 4.6.2, dati Unicode in framework sono stati aggiornati da Unicode standard versione 6.3 alla versione 8.0.  La richiesta di categoria di caratteri Unicode in .NET Framework 4.6.2, alcuni risultati potrebbero non corrispondere i risultati in versioni precedenti di .NET Framework.  Questa modifica principalmente interessa sillabe carattere e segni di vocali carattere Tai lue semplificato: nuovo e ideografici.|
|Suggerimento|Revisione codice e rimuovere/cambiare la logica che varia in base a livello di codice le categorie di caratteri Unicode.|
|Ambito|Secondario|
|Versione|4.6.2|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Char.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.String,System.Int32)?displayProperty=nameWithType></li></ul>|

