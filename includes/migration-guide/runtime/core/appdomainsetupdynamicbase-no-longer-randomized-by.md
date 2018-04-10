### <a name="appdomainsetupdynamicbase-is-no-longer-randomized-by-userandomizedstringhashalgorithm"></a>AppDomainSetup.DynamicBase est aléatoire n’est plus par UseRandomizedStringHashAlgorithm

|   |   |
|---|---|
|Détails|Avant le .NET Framework 4.6, la valeur de <xref:System.AppDomainSetup.DynamicBase> serait aléatoire entre domaines d’application, ou entre processus, si UseRandomizedStringHashAlgorithm a été activée dans le fichier de configuration de l’application. À compter de .NET Framework 4.6, <xref:System.AppDomainSetup.DynamicBase> renvoie un résultat stable entre différentes instances d’une exécution de l’application et entre différents domaines d’application. Bases dynamiques seront toujours différentes pour différentes applications ; Cette modification supprime uniquement l’élément aléatoire d’affectation de noms pour différentes instances de la même application.|
|Suggestion|N’oubliez pas que l’activation <code>UseRandomizedStringHashAlgorithm</code> ne provoque pas de <xref:System.AppDomainSetup.DynamicBase> est aléatoire. Si une base aléatoire est nécessaire, il doit être présenté dans le code de votre application plutôt que via cette API.|
|Portée|Microsoft Edge|
|Version|4.6|
|Type|Runtime|
|API affectées|<ul><li><xref:System.AppDomainSetup.DynamicBase?displayProperty=nameWithType></li></ul>|

