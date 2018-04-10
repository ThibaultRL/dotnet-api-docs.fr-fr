### <a name="etw-eventlisteners-do-not-capture-events-from-providers-with-explicit-keywords-like-the-tpl-provider"></a>ETW EventListeners ne capture pas les événements provenant des fournisseurs avec les mots clés d’explicites (par exemple, le fournisseur de la bibliothèque parallèle de tâches)

|   |   |
|---|---|
|Détails|Les EventListeners ETW avec un masque de mot clé vide ne capturent pas correctement les événements provenant de fournisseurs ayant des mots clés explicites. Dans le .NET Framework 4.5, le fournisseur TPL fournissait des mots clés explicites et provoquait ce problème. Dans le .NET Framework 4.6, les EventListeners ont été mis à jour pour ne plus causer ce problème.|
|Suggestion|Pour contourner ce problème, remplacez les appels à <xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel)> avec les appels à la surcharge EnableEvents qui spécifie explicitement le &quot;tous les mots clés&quot; masque à utiliser : <code>EnableEvents(eventSource, level, unchecked((EventKeywords)0xFFFFffffFFFFffff))</code>. Vous pouvez également, ce problème a été résolu dans le .NET Framework 4.6 et peut être adressé par la mise à niveau vers cette version du .NET Framework.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel)?displayProperty=nameWithType></li></ul>|

