### <a name="systemuriiswellformeduristring-method-returns-false-for-relative-uris-with-a-colon-char-in-first-segment"></a>Méthode de System.Uri.IsWellFormedUriString retourne la valeur false pour les URI relatifs avec un caractère deux-points dans le premier segment

|   |   |
|---|---|
|Détails|À partir de .NET Framework 4.5, <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)> traite les URI relatifs avec un <code>:</code> dans leur premier segment pas bien formé. Il s’agit d’un changement <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name> comportement dans le .NET Framework 4.0 qui a été effectuée pour le rendre conforme à la norme RFC 3986.|
|Suggestion|Cette modification (par exemple, de nombreuses autres modifications URI) affectent uniquement les applications qui ciblent le .NET Framework 4.5 (ou version ultérieur). Pour continuer à utiliser l’ancien comportement, cibler l’application par rapport à .NET Framework 4.0. Vous pouvez également analyser l’URI avant d’appeler <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name> recherchez <code>:</code> caractères que vous pouvez supprimer à des fins de validation, si l’ancien comportement est souhaitable.|
|Portée|Mineur|
|Version|4.5|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=nameWithType></li></ul>|

