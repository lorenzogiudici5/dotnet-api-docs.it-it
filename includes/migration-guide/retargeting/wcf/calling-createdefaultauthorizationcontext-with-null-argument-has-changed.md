### <a name="calling-createdefaultauthorizationcontext-with-a-null-argument-has-changed"></a>Chiamata di CreateDefaultAuthorizationContext con un argomento null è stata modificata

|   |   |
|---|---|
|Dettagli|L'implementazione del <xref:System.IdentityModel.Policy.AuthorizationContext?displayProperty=name> restituito da una chiamata al <xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext(System.Collections.Generic.IList{System.IdentityModel.Policy.IAuthorizationPolicy})?displayProperty=name> con un authorizationPolicies null argomento è cambiata in .NET Framework 4.6.|
|Suggerimento|In rari casi, le app WCF che usano l'autenticazione personalizzata possono riscontrare differenze di comportamento. In questi casi è possibile ripristinare il comportamento precedente in due modi diversi:<ol><li>Ricompilare l'app per destinarla a una versione precedente rispetto a .NET Framework 4.6. Per i servizi ospitati in IIS, usare il &lt;httpRuntime TargetFramework="4.5 =&quot;x.x.&quot;  / &gt; elemento da una versione precedente di .NET Framework di destinazione.</li><li>Aggiungere la riga seguente alla sezione <code>&lt;appSettings&gt;</code> del file app.config: <code>&lt;add key=&quot;appContext.SetSwitch:Switch.System.IdentityModel.EnableCachedEmptyDefaultAuthorizationContext&quot; value=&quot;true&quot; /&gt;</code></li></ol>|
|Ambito|Secondario|
|Versione|4.6|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext(System.Collections.Generic.IList{System.IdentityModel.Policy.IAuthorizationPolicy})?displayProperty=nameWithType></li></ul>|

