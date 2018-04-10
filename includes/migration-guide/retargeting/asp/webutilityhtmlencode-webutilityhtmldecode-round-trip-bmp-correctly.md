### <a name="webutilityhtmlencode-and-webutilityhtmldecode-round-trip-bmp-correctly"></a>WebUtility.HtmlEncode e BMP round trip WebUtility.HtmlDecode correttamente

|   |   |
|---|---|
|Dettagli|Per le applicazioni destinate a .NET Framework 4.5, caratteri che non rientrano correttamente il round trip Basic Multilingual Plane (BMP) quando vengono passati al <xref:System.Net.WebUtility.HtmlDecode(System.String)> metodi.|
|Suggerimento|Questa modifica dovrebbe non hanno alcun effetto sulle applicazioni correnti, ma per ripristinare il comportamento originale, impostare il <code>targetFramework</code> attributo del <code>&lt;httpRuntime&gt;</code> elemento in una stringa diversa da &quot;4.5&quot;. È inoltre possibile impostare gli attributi <code>unicodeEncodingConformance</code> e <code>unicodeDecodingConformance</code> dell'elemento di configurazione <code>&lt;webUtility&gt;</code> per controllare questo comportamento indipendentemente dalla versione di destinazione di .NET Framework.|
|Ambito|Microsoft Edge|
|Versione|4.5|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.Net.WebUtility.HtmlEncode(System.String)?displayProperty=nameWithType></li><li><xref:System.Net.WebUtility.HtmlEncode(System.String,System.IO.TextWriter)?displayProperty=nameWithType></li></ul>|

