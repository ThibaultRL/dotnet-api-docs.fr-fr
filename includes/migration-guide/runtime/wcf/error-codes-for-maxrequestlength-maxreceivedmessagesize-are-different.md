### <a name="error-codes-for-maxrequestlength-or-maxreceivedmessagesize-are-different"></a>Codes d’erreur pour maxRequestLength ou maxReceivedMessageSize sont différents

|   |   |
|---|---|
|Détails|Messages dans WCF services web hébergés dans Internet Information Services (IIS) ou le serveur de développement ASP.NET qui dépassent maxRequestLength (dans ASP.NET) ou maxReceivedMessageSize (dans WCF) ont une erreur autre code d’état HTTP de code hiérarchiqueLes est passé de 400 (demande incorrecte ) à 413 (entité de demande trop grande) et les messages qui dépassent le paramètre maxReceivedMessageSize ou l’attribut maxRequestLength lever un <xref:System.ServiceModel.ProtocolException?displayProperty=name> exception. Cela inclut les cas dans lequel le mode de transfert est transmis en continu.|
|Suggestion|Cette modification facilite le débogage dans les cas où la longueur du message dépasse les limites autorisées par ASP.NET ou WCF. Vous devez modifier tout code qui effectue le traitement basé sur un code d’état HTTP 400.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|

