### <a name="accessing-a-wpf-datagrids-selected-items-from-a-handler-of-the-datagrids-unloadingrow-event-can-cause-a-nullreferenceexception"></a>L’accès aux éléments sélectionnés d’un DataGrid WPF à partir d’un gestionnaire d’événement de UnloadingRow du DataGrid peut provoquer une exception NullReferenceException

|   |   |
|---|---|
|Détails|En raison d’un bogue dans le .NET Framework 4.5, les gestionnaires d’événements pour <xref:System.Windows.Controls.DataGrid> événements liés à la suppression d’une ligne peuvent entraîner un <xref:System.NullReferenceException?displayProperty=name> levée si elles accèdent à la <xref:System.Windows.Controls.DataGrid>de <xref:System.Windows.Controls.Primitives.Selector.SelectedItem?displayProperty=name> ou <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> propriétés.|
|Suggestion|Ce problème a été résolu dans le .NET Framework 4.6 et peut être adressé par la mise à niveau vers cette version du .NET Framework.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Controls.DataGrid.UnloadingRow?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.UnloadingRowDetails?displayProperty=nameWithType></li></ul>|

