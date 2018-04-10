### <a name="missing-target-framework-moniker-results-in-40-behavior"></a>Moniker du Framework cible manquante aboutit au comportement 4.0

|   |   |
|---|---|
|Détails|Applications sans un <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> appliqué à l’assembly au niveau exécuteront automatiquement à l’aide de la sémantique (quirks) de .NET Framework 4.0. Pour garantir la qualité, il est recommandé que tous les fichiers binaires être explicitement attribué avec un <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> indiquant la version du .NET Framework, elles ont été créées avec. Notez qu’à l’aide d’un moniker du framework cible dans un fichier projet cause MSBuild appliquer automatiquement une <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>.|
|Suggestion|A <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> doit être fourni par le biais de l’ajout de l’attribut directement à l’assembly ou en spécifiant une infrastructure cible dans le [fichier de projet ou l’interface utilisateur graphique de propriétés du projet par le biais de Visual Studio](http://blogs.msdn.com/b/visualstudio/archive/2010/05/19/visual-studio- managed-multi-targeting-part-1-concepts-target-framework-moniker-target-framework.aspx).|
|Portée|Majeur|
|Version|4.5|
|Type|Runtime|

