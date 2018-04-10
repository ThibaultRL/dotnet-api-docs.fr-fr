### <a name="intermittently-unable-to-scroll-to-bottom-item-in-itemscontrols-like-listbox-and-datagrid-when-using-custom-datatemplates"></a>Faites défiler vers le dernier élément dans ItemsControls (par exemple, la zone de liste et DataGrid) par intermittence impossible lors de l’utilisation de DataTemplates personnalisé

|   |   |
|---|---|
|Détails|Dans certains cas, un bogue dans le .NET Framework 4.5 est à l’origine ItemsControls (comme <xref:System.Windows.Controls.ListBox?displayProperty=name>, <xref:System.Windows.Controls.ComboBox?displayProperty=name>, <xref:System.Windows.Controls.DataGrid?displayProperty=name>, etc.) pour faire défiler ne pas à leur élément bas lors de l’utilisation de DataTemplates personnalisé. Si le défilement est tenté une deuxième fois (après avoir fait défiler jusqu’en haut), il fonctionnera.|
|Suggestion|Étant donné que ce problème a été résolu dans le .NET Framework 4.5.2, vous pouvez également mettre à niveau votre version du .NET Framework. Vous pouvez également faire glisser les barres de défilement jusqu’au dernier élément de la collection, mais aurez peut-être à recommencer l’opération une deuxième fois pour y arriver.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|

