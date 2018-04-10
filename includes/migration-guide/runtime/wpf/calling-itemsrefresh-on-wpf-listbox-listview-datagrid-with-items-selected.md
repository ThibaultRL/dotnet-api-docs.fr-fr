### <a name="calling-itemsrefresh-on-a-wpf-listbox-listview-or-datagrid-with-items-selected-can-cause-duplicate-items-to-appear-in-the-element"></a>Items.Refresh appel sur un contrôle ListBox de WPF, ListView ou DataGrid avec les éléments sélectionnés peuvent entraîner des éléments en double dans l’élément

|   |   |
|---|---|
|Détails|Dans le .NET Framework 4.5, appeler ListBox.Items.Refresh à partir du code, tandis que les éléments sont sélectionnés dans un <xref:System.Windows.Controls.ListBox?displayProperty=name> peut entraîner les éléments sélectionnés à être dupliqué dans la liste. Un problème similaire se produit avec <xref:System.Windows.Controls.ListView?displayProperty=name> et <xref:System.Windows.Controls.DataGrid?displayProperty=name>. Ce problème a été résolu dans le .NET Framework 4.6.|
|Suggestion|Ce problème peut être contourné en désactivant par programmation des éléments avant <xref:System.Windows.Data.CollectionView.Refresh?displayProperty=name> est appelée, puis ré-en les sélectionnant après la fin de l’appel. Étant donné que ce problème a été résolu dans le .NET Framework 4.6, vous pouvez également mettre à niveau votre version du .NET Framework.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Data.CollectionView.Refresh?displayProperty=nameWithType></li></ul>|

