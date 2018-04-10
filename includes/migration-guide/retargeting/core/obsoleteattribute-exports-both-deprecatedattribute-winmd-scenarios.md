### <a name="obsoleteattribute-exports-as-both-obsoleteattribute-and-deprecatedattribute-in-winmd-scenarios"></a>ObsoleteAttribute Esporta come ObsoleteAttribute sia DeprecatedAttribute negli scenari di WinMD

|   |   |
|---|---|
|Dettagli|Quando si crea una raccolta di metadati Windows (file con estensione winmd), il <xref:System.ObsoleteAttribute?displayProperty=name> attributo viene esportato sia come <xref:System.ObsoleteAttribute?displayProperty=name> e [Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute).|
|Suggerimento|La ricompilazione del codice sorgente esistente che utilizza il <xref:System.ObsoleteAttribute?displayProperty=name> attributo può generare avvisi quando utilizza quel codice da C + + CX o JavaScript.We consiglia di non applicare sia <xref:System.ObsoleteAttribute?displayProperty=name> e [ Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute) al codice negli assembly gestiti, potrebbe verificarsi avvisi di compilazione.|
|Ambito|Microsoft Edge|
|Versione|4.5.1|
|Tipo|Ridestinazione|

