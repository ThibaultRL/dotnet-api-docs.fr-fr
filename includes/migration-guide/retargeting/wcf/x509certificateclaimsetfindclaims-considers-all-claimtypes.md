### <a name="x509certificateclaimsetfindclaims-considers-all-claimtypes"></a>X509CertificateClaimSet.FindClaims considère que tous les claimTypes

|   |   |
|---|---|
|Détails|Dans les applications qui ciblent le .NET Framework 4.6.1, si un ensemble de revendications est initialisé à partir d’un certificat qui a plusieurs entrées DNS de son champ SAN, de X509 la <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name> méthode tente de faire correspondre l’argument claimType avec toutes les entrées DNS. Pour les applications qui ciblent des versions antérieures du .NET Framework, la <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name> méthode tente de faire correspondre l’argument claimType uniquement avec la dernière entrée DNS.|
|Suggestion|Cette modification affecte uniquement les applications qui ciblent le .NET Framework 4.6.1. Cette modification peut être désactivée (ou activée si vous ciblez une version antérieure à 4.6.1) avec le commutateur de compatibilité [DisableMultipleDNSEntries](~/docs/framework/migration-guide/mitigation-x509certificateclaimset-findclaims-method.md#mitigation).|
|Portée|Mineur|
|Version|4.6.1|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=nameWithType></li></ul>|

