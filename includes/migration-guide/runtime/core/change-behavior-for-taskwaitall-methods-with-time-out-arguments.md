### <a name="change-in-behavior-for-taskwaitall-methods-with-time-out-arguments"></a>Modification du comportement pour les méthodes Task.WaitAll avec des arguments de délai d’attente

|   |   |
|---|---|
|Détails|Task.WaitAll comportement a été rendu plus cohérent dans .NET 4.5.In .NET Framework 4, ces méthodes se comportaient de manière incohérente. Lorsque le délai d'attente expirait, si une ou plusieurs tâches étaient terminées ou annulées avant l'appel de la méthode, la méthode levait une exception <xref:System.AggregateException?displayProperty=name>. Lorsque le délai d’attente expirait, si aucune tâche n’était terminée ou annulée avant l’appel de la méthode alors qu’une ou plusieurs tâches adoptaient ces états après l’appel de la méthode, la méthode retournait la valeur false.<br/><br/>Dans le .NET Framework 4.5, ces surcharges de méthode retournent désormais false si toutes les tâches sont toujours en cours d’exécution lors de l’intervalle de délai d’attente a expiré, et elles ne lèvent une <xref:System.AggregateException?displayProperty=name> exception uniquement si une tâche d’entrée a été annulée (qu’il s’agisse d’avant ou après la méthode Appelez) et aucuns autres tâches ne sont en cours d’exécution.|
|Suggestion|Si un <xref:System.AggregateException?displayProperty=name> qui est interceptée comme un moyen de détecter une tâche qui a été annulée avant l’appel de WaitAll appelé que code doit effectuer à la place de la détection même via la propriété IsCanceled (par exemple :. Any(t =&gt; t.IsCanceled)) depuis le .NET 4.6 lèvera uniquement dans ce cas si toutes les tâches attendues sont terminées avant le délai d’attente.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32,System.Threading.CancellationToken)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.TimeSpan)?displayProperty=nameWithType></li></ul>|

