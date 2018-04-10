### <a name="some-workflow-drag-and-drop-apis-are-obsolete"></a>Certaines API de glisser-déplacer de flux de travail est obsolètes

|   |   |
|---|---|
|Détails|Cette API de glisser-déplacer de flux de travail est obsolète et génère des avertissements du compilateur si l’application est reconstruite à partir de 4.5.|
|Suggestion|Nouvelle <xref:System.Activities.Presentation.DragDropHelper?displayProperty=name> API qui prennent en charge les opérations avec plusieurs objets doivent être utilisées à la place. Vous pouvez également supprimer les avertissements de génération ou les éviter en utilisant un compilateur plus ancien. Ces API sont toujours prises en charge.|
|Portée|Mineur|
|Version|4.5|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Activities.Presentation.DragDropHelper.DoDragMove(System.Activities.Presentation.WorkflowViewElement,System.Windows.Point)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetCompositeView(System.Windows.DragEventArgs)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetDraggedModelItem(System.Windows.DragEventArgs)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetDroppedObject(System.Windows.DependencyObject,System.Windows.DragEventArgs,System.Activities.Presentation.EditingContext)?displayProperty=nameWithType></li></ul>|

