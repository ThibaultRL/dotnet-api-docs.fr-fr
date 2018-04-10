### <a name="wpf-spell-checking-fails-in-unexpected-ways"></a>La correction orthographique dans WPF échoue de façon inattendue

|   |   |
|---|---|
|Détails|Cela inclut un nombre de problèmes de vérificateur d’orthographe WPF :<ul><li>Vérificateur d’orthographe WPF lève parfois <xref:System.Runtime.InteropServices.COMException?displayProperty=name></li><li>Vérificateur d’orthographe WPF échoue avec <xref:System.UnauthorizedAccessException> lorsque les applications sont lancées à l’aide de « exécuter en tant qu’utilisateur différent »</li><li>Vérificateur d’orthographe WPF identifie incorrectement les fautes d’orthographe dans les mots composés comme 'Hausnummer' en allemand.</li></ul>|
|Suggestion|Problème #1 : ce problème a été corrigé dans .NET Framework 4.6.2 problème n° 2 - vérificateur orthographique de WPF n’est plus pris en charge lorsque les applications sont lancées à l’aide de « exécuter en tant qu’utilisateur différent ». À partir de .NET Framework 4.6.2, applications lancées de cette manière ne seront bloquent plus inattendu : à la place le vérificateur d’orthographe va être désactivé en mode silencieux. Problème #3 - ce problème a été corrigé dans .NET Framework 4.6.2.|
|Portée|Microsoft Edge|
|Version|4.6.1|
|Type|Runtime|

