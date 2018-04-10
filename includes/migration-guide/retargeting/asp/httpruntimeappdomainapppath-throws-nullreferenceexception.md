### <a name="httpruntimeappdomainapppath-throws-a-nullreferenceexception"></a>HttpRuntime.AppDomainAppPath lève une exception NullReferenceException

|   |   |
|---|---|
|Détails|Dans le .NET Framework 4.6.2, le runtime lève une <code>T:System.NullReferenceException</code> lorsque vous récupérez un <code>P:System.Web.HttpRuntime.AppDomainAppPath</code> valeur qui inclut des caractères null. Dans le .NET Framework 4.6.1 et versions antérieures, le runtime lève une <code>T:System.ArgumentNullException</code>.|
|Suggestion|Vous pouvez procéder de la suite pour répondre à cette modification :<ul><li>Gérer le <code>T:System.NullReferenceException</code> si votre application est en cours d’exécution sur le .NET Framework 4.6.2.</li><li>Mise à niveau vers la 4.7 .NET Framework, qui rétablit le comportement précédent et lève un <code>T:System.ArgumentNullException</code>.</li></ul>|
|Portée|Microsoft Edge|
|Version|4.6.2|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Web.HttpRuntime.AppDomainAppPath?displayProperty=nameWithType></li></ul>|

