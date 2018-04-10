### <a name="listsort-algorithm-changed"></a>Algorithme List.Sort modifié

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.5, <xref:System.Collections.Generic.List%601?displayProperty=name>d’algorithme de tri a changé (pour un tri approfondie au lieu d’un tri rapide). <xref:System.Collections.Generic.List%601?displayProperty=name>de tri n’a jamais été stable, mais cette modification peut provoquer des différents scénarios trier les manières instable. Cela signifie simplement que des éléments équivalents peuvent effectuer un tri dans des ordres différents dans les appels suivants de l’API.|
|Suggestion|Étant donné que l’ancien algorithme de tri a été également instable (bien que de manière légèrement différente), il ne doit y avoir aucun code qui dépend des éléments équivalents toujours tri dans un ordre particulier. S’il existe des instances de code en fonction de qui et de chance avec l’ancien comportement, ce code doit être mis à jour pour utiliser un comparateur qui sera de façon déterministe triez les éléments dans l’ordre souhaité.|
|Portée|Transparent|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Collections.Generic.List%601.Sort?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Comparison{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Int32,System.Int32,System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li></ul>|

