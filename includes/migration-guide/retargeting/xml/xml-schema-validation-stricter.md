### <a name="xml-schema-validation-is-stricter"></a>Validation de schéma XML est plus stricte

|   |   |
|---|---|
|Détails|Dans le .NET Framework 4.5, la validation de schéma XML est plus stricte. Si vous utilisez xsd:anyURI pour valider un URI tel qu'un protocole mailto, la validation échoue si l'URI contient des espaces. Dans les versions antérieures du .NET Framework, la validation réussissait. La modification affecte uniquement les applications qui ciblent le .NET Framework 4.5.|
|Suggestion|Si un contrôle de .NET Framework 4.0 est nécessaire, l’application de validation peut cibler la version 4.0 de .NET Framework. Lorsque le reciblage vers .NET 4.5, toutefois, révision du code doit être effectuée pour vous assurer que les URI non valide (avec espaces) ne doivent pas en tant que valeurs d’attribut avec le type de données anyURI.|
|Portée|Mineur|
|Version|4.5|
|Type|Reciblage|

