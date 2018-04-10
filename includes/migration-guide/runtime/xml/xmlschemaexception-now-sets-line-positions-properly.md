### <a name="xmlschemaexception-now-sets-line-positions-properly"></a>XmlSchemaException maintenant définit les positions de ligne correctement

|   |   |
|---|---|
|Détails|Si le <xref:System.Xml.Linq.LoadOptions.SetLineInfo> valeur est passée à la méthode de charge et une erreur de validation se produit, le <xref:System.Xml.Schema.XmlSchemaException.LineNumber> et <xref:System.Xml.Schema.XmlSchemaException.LinePosition> propriétés contiennent désormais les informations de ligne.|
|Suggestion|Code de gestion des exceptions qui suppose <xref:System.Xml.Schema.XmlSchemaException.LineNumber> et <xref:System.Xml.Schema.XmlSchemaException.LinePosition> ne sera pas jeu doit être mis à jour, car ces propriétés seront désormais être définies correctement lorsque SetLineInfo est utilisé lors du chargement XML.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Xml.Linq.LoadOptions.SetLineInfo?displayProperty=nameWithType></li></ul>|

