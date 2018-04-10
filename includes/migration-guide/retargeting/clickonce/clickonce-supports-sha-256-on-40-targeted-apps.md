### <a name="clickonce-supports-sha-256-on-40-targeted-apps"></a>ClickOnce prend en charge SHA-256 sur les applications ciblées 4.0

|   |   |
|---|---|
|Détails|Auparavant, une application ClickOnce avec un certificat signé avec SHA-256 nécessite .NET 4.5 ou version ultérieure pour être présent, même si l’application cible 4.0. À présent, que les applications de ClickOnce ciblés 4.0 peuvent s’exécuter sur 4.0, même si signés avec SHA-256.|
|Suggestion|Cette modification supprime cette dépendance et permet aux certificats SHA-256 être utilisé pour signer des applications ClickOnce qui ciblent .NET Framework 4 et versions antérieures.|
|Portée|Mineur|
|Version|4.6|
|Type|Reciblage|

