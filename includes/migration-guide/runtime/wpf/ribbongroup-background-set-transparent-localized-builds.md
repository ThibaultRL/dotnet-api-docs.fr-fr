### <a name="ribbongroup-background-is-set-to-transparent-in-localized-builds"></a>Arrière-plan de RibbonGroup est défini sur transparent dans les versions localisées

|   |   |
|---|---|
|Détails|<xref:System.Windows.Controls.Ribbon.RibbonGroup?displayProperty=name> en arrière-plan sur les versions localisées était toujours dessiné avec pinceau Transparent, ce qui entraîne une mauvaise expérience d’interface utilisateur. Il est résolu dans .NET 4,7 correctif WPF en mettant à jour les ressources localisées pour <xref:System.Windows.Controls.Ribbon.RibbonGroup?displayProperty=name>, qui à son tour permet de s’assurer que le pinceau correct est sélectionné.|
|Suggestion|Mise à niveau vers .NET 4.7|
|Portée|Microsoft Edge|
|Version|4.6.2|
|Type|Runtime|

