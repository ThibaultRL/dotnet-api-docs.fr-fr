### <a name="netdatacontractserializer-fails-to-deserialize-a-concurrentdictionary-serialized-with-a-different-net-version"></a>NetDataContractSerializer ne parvient pas à la désérialisation d’un ConcurrentDictionary sérialisé avec une autre version de .NET

|   |   |
|---|---|
|Détails|Par défaut, le <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> peut être utilisé uniquement si la sérialisation et désérialisation se termine partagent les mêmes types CLR. Par conséquent, il n’est pas garanti qu’un objet sérialisé avec une version du .NET Framework pouvant être désérialisé par une autre version.<xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> est un type qui est connu pour ne pas à désérialiser correctement si sérialisé avec le .NET Framework 4.5 ou version antérieure et désérialisé avec le .NET Framework 4.5.1 ou version ultérieure.|
|Suggestion|Il existe un certain nombre de contournement possible pour résoudre ce problème :<ul><li>Mise à niveau de l’ordinateur de sérialisation pour utiliser .NET Framework 4.5.1, également.</li><li>Utilisez <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> au lieu de <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> comme il n’attend pas les mêmes types exacts de CLR à la sérialisation et de désérialisation se termine.</li><li>Utilisez <xref:System.Collections.Generic.Dictionary%602?displayProperty=name> au lieu de <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> , car il ne présente pas cette 4.5 particuliers -&gt;4.5.1 break.</li></ul>|
|Portée|Mineur|
|Version|4.5.1|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Runtime.Serialization.NetDataContractSerializer.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li></ul>|

