### <a name="unicode-standard-version-80-categories-now-supported"></a>Catégories Unicode standard version 8.0 maintenant pris en charge

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.6.2, les données Unicode dans le framework a été mis à Unicode standard version 6.3 vers la version 8.0.  Lors de la demande de catégorie de caractères Unicode dans le .NET Framework 4.6.2, certains résultats ne peuvent pas correspondre les résultats dans les versions précédentes du .NET Framework.  Cette modification principalement affecte Cherokee syllabes et se connecte de nouveau TAÏ LÜ voyelles et marques d’accentuation.|
|Suggestion|Passez en revue le code et supprimer/modifier la logique qui varie selon les catégories de caractères Unicode codé en dur.|
|Portée|Mineur|
|Version|4.6.2|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Char.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.String,System.Int32)?displayProperty=nameWithType></li></ul>|

