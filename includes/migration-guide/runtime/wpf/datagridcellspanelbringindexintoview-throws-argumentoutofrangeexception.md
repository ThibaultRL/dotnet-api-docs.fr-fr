### <a name="datagridcellspanelbringindexintoview-throws-argumentoutofrangeexception"></a>DataGridCellsPanel.BringIndexIntoView throws ArgumentOutOfRangeException

|   |   |
|---|---|
|Détails|<xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)> fonctionne de façon asynchrone si la virtualisation des colonnes est activée, mais les largeurs de colonne n’ont pas encore été déterminés.  Si les colonnes sont supprimés avant que le travail asynchrone se produit, un <xref:System.ArgumentOutOfRangeException?displayProperty=name> peut se produire.|
|Suggestion|L’une des opérations suivantes :<ol><li>Mise à niveau vers .NET 4.7.</li><li>Installez le correctif dernière maintenance pour .NET 4.6.2.</li><li>Éviter la suppression de colonnes jusqu'à ce que la réponse asynchrone à <xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)> est terminée.</li></ol>|
|Portée|Microsoft Edge|
|Version|4.6.2|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object,System.Windows.Controls.DataGridColumn)?displayProperty=nameWithType></li></ul>|

