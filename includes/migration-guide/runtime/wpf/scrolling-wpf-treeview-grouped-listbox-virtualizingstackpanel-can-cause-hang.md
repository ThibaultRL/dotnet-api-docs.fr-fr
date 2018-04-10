### <a name="scrolling-a-wpf-treeview-or-grouped-listbox-in-a-virtualizingstackpanel-can-cause-a-hang"></a>Défilement un TreeView WPF ou une ListBox groupée dans un VirtualizingStackPanel peut provoquer un blocage

|   |   |
|---|---|
|Détails|Dans le .NET Framework 4.5, le défilement WPF <xref:System.Windows.Controls.TreeView?displayProperty=name> dans une pile virtualisée Panneau de configuration peut provoquer des blocages s’il existe des marges dans la fenêtre d’affichage (entre les éléments dans le <xref:System.Windows.Controls.TreeView?displayProperty=name>, par exemple, ou sur un élément ItemsPresenter). En outre, dans certains cas, des éléments de taille différente dans une même vue peuvent causer une instabilité, même s’il n’y a pas de marges.|
|Suggestion|Vous pouvez éviter ce problème en effectuant une mise à niveau vers .NET Framework 4.5.1. Vous pouvez également les marges peuvent être supprimés à partir de l’affichage de collections (comme <xref:System.Windows.Controls.TreeView?displayProperty=name>s) au sein de la pile virtualisé panneaux si tous les éléments contenus est de même taille.|
|Portée|Majeur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Controls.VirtualizingStackPanel.SetIsVirtualizing(System.Windows.DependencyObject,System.Boolean)?displayProperty=nameWithType></li></ul>|

