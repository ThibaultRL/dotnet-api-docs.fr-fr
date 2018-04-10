### <a name="flowdocument-may-show-an-extra-line-of-text"></a>FlowDocument peut afficher une ligne de texte supplémentaire

|   |   |
|---|---|
|Détails|Dans certains cas, un <xref:System.Windows.Documents.FlowDocument> élément affiche une ligne de texte supplémentaire lors de l’exécution sur le .NET Framework 4.5 par rapport à la façon dont il affiché lors de l’exécuter sur le .NET Framework 4.0. Aucun cas connus de la modification à l’origine de n’importe quel texte à afficher de façon illisible ou mal, mais peut amener texte qui précédemment a été omis dans un <xref:System.Windows.Documents.FlowDocument>de l’afficher.|
|Suggestion|Dans certains cas, le diminuent PageHeight, propriété de l’élément de l’affichage d’une permettre restaurer le nombre de lignes affichées précédentes.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Documents.FlowDocument.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Documents.FlowDocument.%23ctor(System.Windows.Documents.Block)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentReader.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentPageViewer.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.DocumentPageView.%23ctor?displayProperty=nameWithType></li></ul>|

