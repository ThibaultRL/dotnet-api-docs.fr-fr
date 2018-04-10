### <a name="wpf-dispatchersynchronizationcontextcreatecopy-now-returns-a-new-copy-instead-of-the-current-instance"></a>WPF DispatcherSynchronizationContext.CreateCopy retourne désormais une nouvelle copie au lieu de l’instance actuelle

|   |   |
|---|---|
|Détails|Dans le .NET Framework 4, <xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy> renvoyé une référence à l’instance actuelle, principalement comme une optimisation des performances. Dans le .NET Framework 4.5, il retourne une nouvelle instance, ce qui permet, pour la première fois, de conclure que les références égales indiquent que le thread en cours d’exécution se trouve dans le bon contexte de synchronisation.  Il est peu probable que le code qui vérifie l’identité de ces références est affecté, mais en raison de la modification, le code qui appelle la méthode <xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy> doivent être testées dans le cadre de la migration vers .NET Framework 4.5 ou une version ultérieure.|
|Suggestion|N’oubliez pas que <xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy> retournent désormais un nouveau <xref:System.Threading.SynchronizationContext?displayProperty=name> objet. Avant, le code qui utilisait l’équivalence des références générées de cette manière ne vérifiait pas réellement si le contexte était approprié. À présent, avec le .NET 4.5 et ultérieur, le contexte est bien vérifié.  Bien que cela soit peu susceptible de provoquer des problèmes, l’utilisation des chemins de code concernés doit suffire à déterminer si cela peut poser un problème.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy?displayProperty=nameWithType></li></ul>|

