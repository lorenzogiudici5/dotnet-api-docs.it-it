### <a name="assemblies-compiled-with-regexcompiletoassembly-breaks-between-40-and-45"></a>Assembly compilati con interruzioni di pagina Regex.CompileToAssembly 4.0 e 4.5

|   |   |
|---|---|
|Dettagli|Se si compila un assembly di espressioni regolari compilate con di .NET Framework 4.5, ma è destinato a .NET Framework 4, tenta di utilizzare una delle espressioni regolari in assembly in un sistema con .NET Framework 4 è installato genera un'eccezione.|
|Suggerimento|Per risolvere il problema, è possibile eseguire una delle operazioni seguenti:<ul><li>Compilare l'assembly che contiene le espressioni regolari con .NET Framework 4.</li><li>Usare un'espressione regolare interpretata.</li></ul>|
|Ambito|Secondario|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName)?displayProperty=nameWithType></li><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName,System.Reflection.Emit.CustomAttributeBuilder[])?displayProperty=nameWithType></li><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName,System.Reflection.Emit.CustomAttributeBuilder[],System.String)?displayProperty=nameWithType></li></ul>|

