### <a name="soapformatter-cannot-deserialize-hashtable-and-similar-ordered-collection-objects"></a>Impossible de désérialiser la table de hachage SoapFormatter et ordonnée semblables objets de collection

|   |   |
|---|---|
|Détails|Le <xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> fait pas la garantie que les objets sérialisés sous une version du .NET Framework sera désérialiser correctement sous une version différente. Plus précisément, certaines collections ordonnées (comme <xref:System.Collections.Hashtable?displayProperty=name>) ajouté des membres entre 4.0 et 4.5 telles que les objets de ces types ne peut pas désérialiser avec .NET 4.0, si elles ont été sérialisées avec le .NET 4.5. Notez que si les données sérialisées sont sérialisées et désérialisées avec la même version du .NET Framework, aucun problème ne se produit.|
|Suggestion|<xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> sérialisation doit être remplacée par <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> sérialisation ou <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> pour qu’elles soient résistantes aux modifications du .NET Framework.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object,System.Runtime.Remoting.Messaging.Header[])?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream,System.Runtime.Remoting.Messaging.HeaderHandler)?displayProperty=nameWithType></li></ul>|

