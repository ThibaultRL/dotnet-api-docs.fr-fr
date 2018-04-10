### <a name="some-net-apis-cause-first-chance-handled-entrypointnotfoundexceptions"></a>Certaines API .NET cause première chance (géré) EntryPointNotFoundExceptions

|   |   |
|---|---|
|Détails|Dans le .NET Framework 4.5, un petit nombre de méthodes .NET a commencé lever de première chance <xref:System.EntryPointNotFoundException?displayProperty=name>s. Ces exceptions étaient gérées dans le .NET Framework, mais pouvaient arrêter l’automatisation des tests, car celle-ci ne s’attendait pas à des exceptions de première chance. Ces mêmes API provoquent l’arrêt de certaines exécutions ApiVerifier lorsque HighVersionLie est activé.|
|Suggestion|Vous pouvez éviter ce problème en effectuant une mise à niveau vers .NET Framework 4.5.1. Vous pouvez également automatisation de test peut être mis à jour pour ne pas arrêter de première chance <xref:System.EntryPointNotFoundException?displayProperty=name>s.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Diagnostics.Debug.Assert(System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String,System.String)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String,System.String,System.Object[])?displayProperty=nameWithType></li><li><xref:System.Xml.Serialization.XmlSerializer.%23ctor(System.Type)?displayProperty=nameWithType></li></ul>|

