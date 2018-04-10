### <a name="wpf-datatemplate-elements-are-now-visible-to-uia"></a>WPF DataTemplate éléments sont désormais visibles par UIA

|   |   |
|---|---|
|Détails|Auparavant, <xref:System.Windows.DataTemplate?displayProperty=name> éléments ont été invisibles dans UI Automation. À compter de la version 4.5, UI Automation détecte ces éléments. Cela est utile dans de nombreux cas, mais peut provoquer des problèmes des tests qui dépendent des arborescences UIA ne contenant ne pas <xref:System.Windows.DataTemplate?displayProperty=name> éléments.|
|Suggestion|Tests d’UI Automation pour cette application peut avoir besoin mis à jour pour prendre en compte pour l’arborescence UIA maintenant notamment précédemment invisible <xref:System.Windows.DataTemplate?displayProperty=name> éléments. Par exemple, les tests qui attendent des éléments contigus doivent maintenant s’attendre à ce que des éléments UIA, autrefois indétectables, se trouvent entre ces éléments. Autre exemple : Les tests qui reposent sur certains nombres ou index pour les éléments UIA peuvent nécessiter la modification de leurs valeurs.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.DataTemplate.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.DataTemplate.%23ctor(System.Object)?displayProperty=nameWithType></li></ul>|

