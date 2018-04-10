### <a name="dataobjectgetdata-now-retrieves-data-as-utf-8"></a>DataObject.GetData maintenant récupère les données au format UTF-8

|   |   |
|---|---|
|Détails|Pour les applications qui ciblent le .NET Framework 4 ou qui s’exécutent sur .NET Framework 4.5.1 ou des versions antérieures, <code>DataObject.GetData</code> récupère les données au format HTML sous forme de chaîne ASCII. Par conséquent, les caractères non-ASCII (caractères dont les codes ASCII sont supérieurs à 0x7F) sont représentés par deux caractères aléatoires. Pour les applications qui ciblent le .NET Framework 4.5 ou version ultérieur et s’exécutent sur le .NET Framework 4.5.2 <code>DataObject.GetData</code> récupère des données au format HTML en tant que UTF-8, qui représente correctement les caractères supérieurs à 0x7F.|
|Suggestion|Si vous avez implémenté une solution de contournement pour ce problème de codage des chaînes au format HTML (par exemple, en codant explicitement la chaîne HTML récupérée à partir du Presse-papiers en la passant à <xref:System.Text.UTF8Encoding.GetString(System.Byte[],System.Int32,System.Int32)?displayProperty=name>) et que vous reciblez votre application à partir de la version 4 et 4.5, qui solution de contournement doit être supprimée. Si l’ancien comportement est nécessaire pour une raison quelconque, l’application peut cibler .NET Framework 4.0 pour obtenir ce comportement.|
|Portée|Microsoft Edge|
|Version|4.5.2|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Windows.DataObject.GetData(System.String)?displayProperty=nameWithType></li><li><xref:System.Windows.DataObject.GetData(System.Type)?displayProperty=nameWithType></li><li><xref:System.Windows.DataObject.GetData(System.String,System.Boolean)?displayProperty=nameWithType></li></ul>|

