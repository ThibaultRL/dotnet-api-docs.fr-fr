### <a name="enumerableemptylttresultgt-always-returns-cached-instance"></a>Enumerable.Empty&lt;TResult&gt; toujours retourne mises en cache l’instance

|   |   |
|---|---|
|Détails|À compter de .NET 4.5, <xref:System.Linq.Enumerable.Empty%60%601> retourne toujours une instance interne mise en cache <xref:System.Collections.Generic.IEnumerable%601>. Auparavant, <xref:System.Linq.Enumerable.Empty%60%601> serait cache vide <xref:System.Collections.Generic.IEnumerable%601> au moment de l’API a été appelée, ce qui signifie que dans certaines conditions dans lesquelles <xref:System.Linq.Enumerable.Empty%60%601> a été appelé rapidement et simultanément, différentes instances du type peuvent être retournés pour les différents appels à la API.|
|Suggestion|Étant donné que l’ancien comportement était non déterministe, il est peu probable que le code en dépende. Toutefois, dans le cas peu probable où des énumérables vides sont comparés et supposés être parfois inégaux, vous devez créer des tableaux vides explicites (<code>new T[0]</code>) au lieu d’utiliser <xref:System.Linq.Enumerable.Empty%60%601>.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Linq.Enumerable.Empty%60%601?displayProperty=nameWithType></li></ul>|

