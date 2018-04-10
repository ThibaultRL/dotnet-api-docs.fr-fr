### <a name="calling-datagridcommitedit-from-a-celleditending-handler-drops-focus"></a>Appel de DataGrid.CommitEdit à partir d’un gestionnaire CellEditEnding supprime le focus

|   |   |
|---|---|
|Détails|Appel <xref:System.Windows.Controls.DataGrid.CommitEdit> à partir d’un de la <xref:System.Windows.Controls.DataGrid?displayProperty=name>de <xref:System.Windows.Controls.DataGrid.CellEditEnding?displayProperty=name> provoque des gestionnaires d’événements le <xref:System.Windows.Controls.DataGrid?displayProperty=name> à perd le focus.|
|Suggestion|Ce bogue a été résolu dans le .NET Framework 4.5.2. Vous pouvez donc l’éviter en mettant à niveau votre version du .NET Framework. Sinon, il peut être évité explicitement en sélectionnant à nouveau la <xref:System.Windows.Controls.DataGrid?displayProperty=name> après l’appel <xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=name>.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.CommitEdit(System.Windows.Controls.DataGridEditingUnit,System.Boolean)?displayProperty=nameWithType></li></ul>|

