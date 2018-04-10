### <a name="ipad-should-not-be-used-in-custom-capabilities-file-because-it-is-now-a-browser-capability"></a>IPad ne doit pas servir dans le fichier de fonctionnalités personnalisées, car il est désormais une fonctionnalité du navigateur

|   |   |
|---|---|
|Détails|À compter de .NET 4.5, iPad étant un identificateur dans le fichier des fonctionnalités du navigateur ASP.NET par défaut, il ne doit pas être utilisé dans un fichier de fonctionnalités personnalisés|
|Suggestion|Si des fonctionnalités spécifiques à l’iPad sont requises, il est nécessaire de modifier le comportement d’iPad en définissant des fonctionnalités sur la passerelle prédéfinis refID &quot;IPad&quot; au lieu d’en générant un nouveau &quot;IPad&quot; ID de l’agent utilisateur mise en correspondance.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|

