### <a name="obsoleteattribute-exports-as-both-obsoleteattribute-and-deprecatedattribute-in-winmd-scenarios"></a>ObsoleteAttribute exporte comme ObsoleteAttribute et DeprecatedAttribute dans les scénarios de WinMD

|   |   |
|---|---|
|Détails|Lorsque vous créez une bibliothèque de métadonnées Windows (fichier .winmd), le <xref:System.ObsoleteAttribute?displayProperty=name> attribut est exporté en tant que les deux <xref:System.ObsoleteAttribute?displayProperty=name> et [Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute).|
|Suggestion|La recompilation de code source existant qui utilise le <xref:System.ObsoleteAttribute?displayProperty=name> attribut peut générer des avertissements lors de l’utilisation de ce code à partir de C + c++ / CX ou JavaScript.We déconseillons d’appliquer à la fois <xref:System.ObsoleteAttribute?displayProperty=name> et [ Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute) au code dans les assemblys managés ; il peut générer des avertissements de build.|
|Portée|Microsoft Edge|
|Version|4.5.1|
|Type|Reciblage|

