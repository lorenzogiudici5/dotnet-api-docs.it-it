### <a name="x509certificateclaimsetfindclaims-considers-all-claimtypes"></a>ClaimType considera tutti X509CertificateClaimSet.FindClaims

|   |   |
|---|---|
|Dettagli|Nelle App destinate a .NET Framework 4.6.1, se un'attestazione set X509 viene inizializzato da un certificato con più voci DNS nel proprio campo SAN, il <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name> metodo tenta di ottenere l'argomento claimType con tutte le voci DNS. Per le app destinate alle versioni precedenti di .NET Framework, il <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name> metodo tenta di ottenere l'argomento claimType solo con l'ultima voce DNS.|
|Suggerimento|Questa modifica riguarda solo le applicazioni destinate a .NET Framework 4.6.1. Questa modifica potrebbe essere disabilitata (o abilitata se la destinazione è una versione precedente alla 4.6.1) con l'opzione di compatibilità [DisableMultipleDNSEntries](~/docs/framework/migration-guide/mitigation-x509certificateclaimset-findclaims-method.md#mitigation).|
|Ambito|Secondario|
|Versione|4.6.1|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=nameWithType></li></ul>|

