### <a name="deserialization-of-objects-across-appdomains-can-fail"></a>La deserializzazione di oggetti tra domini di applicazione può non riuscire

|   |   |
|---|---|
|Dettagli|In alcuni casi, quando un'app usa due o più domini di app con diverse basi dell'applicazione, il tentativo di deserializzare gli oggetti nel contesto di una chiamata logica tra domini di app genera un'eccezione.|
|Suggerimento|Vedere [attenuazione: deserializzazione di oggetti tra domini App](~/docs/framework/migration-guide/mitigation-deserialization-of-objects-across-app-domains.md)|
|Ambito|Microsoft Edge|
|Versione|4.5.1|
|Tipo|Runtime|

