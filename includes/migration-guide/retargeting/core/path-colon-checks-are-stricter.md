### <a name="path-colon-checks-are-stricter"></a>Vérifications de deux points de chemin d’accès sont plus strictes

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.6.2, un nombre de modifications ont été apporté pour prendre en charge les chemins d’accès précédemment non pris en charge (à la fois dans la longueur et le format). Vérifie la syntaxe de séparateur (deux-points) de lecteur adéquate ont été apportées plus approprié, qui a comme effet secondaire de bloquer certains chemins d’accès de l’URI dans quelques sélectionnez API de chemin d’accès où ils utilisés pour être tolérée.|
|Suggestion|Si la transmission d’un URI à l’API affecté, modifiez la chaîne pour d’abord être un chemin d’accès valide.<ul><li>Supprimer le modèle à partir de l’URL manuellement (par exemple, supprimez <code>file://</code> à partir d’URL)</li><li>Passez l’URI pour la <xref:System.Uri> classe et utiliser <xref:System.Uri.LocalPath></li></ul>Ou bien, vous pouvez désactiver la normalisation de chemin d’accès de nouveau en définissant le <code>Switch.System.IO.UseLegacyPathHandling</code> commutateur AppContext sur true.|
|Portée|Microsoft Edge|
|Version|4.6.2|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.IO.Path.GetDirectoryName(System.String)?displayProperty=nameWithType></li><li><xref:System.IO.Path.GetPathRoot(System.String)?displayProperty=nameWithType></li></ul>|

