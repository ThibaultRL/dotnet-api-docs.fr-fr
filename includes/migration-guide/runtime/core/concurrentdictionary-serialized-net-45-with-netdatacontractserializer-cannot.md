### <a name="a-concurrentdictionary-serialized-in-net-45-with-netdatacontractserializer-cannot-be-deserialized-by-net-451-or-452"></a>Un ConcurrentDictionary sérialisé dans .NET 4.5 avec NetDataContractSerializer ne peut pas être désérialisé par .NET 4.5.1 ou 4.5.2

|   |   |
|---|---|
|Détails|En raison de changements internes pour le type, <xref:System.Collections.Concurrent.ConcurrentDictionary%602> les objets qui sont sérialisés avec le .NET Framework 4.5 à l’aide de la <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> ne peut pas être désérialisé dans le .NET Framework 4.5.1 ou dans le .NET Framework 4.5.2.Note ce déplacement dans l’autre (direction sérialisation avec le .NET Framework 4.5.x et la désérialisation avec le .NET Framework 4.5) fonctionne. De même, ensemble de la sérialisation entre les versions 4.x fonctionne avec le .NET Framework 4.6.Serializing et la désérialisation avec une seule version du .NET Framework n’est pas affectée.|
|Suggestion|S’il est nécessaire sérialiser et désérialiser un <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> entre le .NET Framework 4.5 et le .NET Framework 4.5.1/4.5.2, comme un autre sérialiseur le <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> ou <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> sérialiseur doit être utilisé à la place de la <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>. Vous pouvez également, car ce problème est résolu dans le .NET Framework 4.6, il peut être résolu par la mise à niveau vers cette version du .NET Framework.|
|Portée|Mineur|
|Version|4.5.1|
|Type|Runtime|

