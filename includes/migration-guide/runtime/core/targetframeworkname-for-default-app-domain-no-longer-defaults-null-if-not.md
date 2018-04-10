### <a name="targetframeworkname-for-default-app-domain-no-longer-defaults-to-null-if-not-set"></a>TargetFrameworkName pour le domaine d’application par défaut n’est plus valeur par défaut est null si n’est pas définie

|   |   |
|---|---|
|Détails|Le <xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> a été précédemment null dans le domaine d’application par défaut, sauf si elle a été définie explicitement. À compter de 4.6, la <xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> propriété pour le domaine d’application par défaut a une valeur par défaut dérivée TargetFrameworkAttribute (le cas échéant). Domaines d’application par défaut non continue à hériter leurs <xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> à partir du domaine d’application par défaut (qui pas par défaut est null dans la version 4.6) sauf si elle est explicitement substituée.|
|Suggestion|Le code doit être mis à jour pour ne pas attendre que <xref:System.AppDomainSetup.TargetFrameworkName> ait la valeur Null par défaut. Si vous avez besoin que cette propriété continue de prendre la valeur Null, vous pouvez la définir explicitement sur cette valeur.|
|Portée|Microsoft Edge|
|Version|4.6|
|Type|Runtime|
|API affectées|<ul><li><xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=nameWithType></li></ul>|

