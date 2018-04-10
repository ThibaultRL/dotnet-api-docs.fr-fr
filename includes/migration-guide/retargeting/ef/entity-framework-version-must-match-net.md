### <a name="entity-framework-version-must-match-the-net-framework-version"></a>Version de Framework l’entité doit correspondre à la version de .NET Framework

|   |   |
|---|---|
|Détails|La version de framework entité doit correspondre à la version du .NET framework. Entity Framework 5 est recommandée pour le .NET 4.5. Il existe des problèmes connus avec EF 4.x dans un projet .NET 4.5 autour de <xref:System.ComponentModel.DataAnnotations>. Dans .NET 4.5, ils ont été déplacés vers un autre assembly, afin de déterminer les annotations à utiliser des problèmes.|
|Suggestion|Mise à niveau vers Entity Framework 5 pour .NET Framework 4.5|
|Portée|Majeur|
|Version|4.5|
|Type|Reciblage|

