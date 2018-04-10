### <a name="rsacngverifyhash-now-returns-false-for-any-verification-failure"></a>RSACng.VerifyHash renvoie maintenant la valeur False pour tout échec de vérification

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.6.2, cette méthode retourne <strong>False</strong> si la signature proprement dite est incorrect. Elle retourne false pour tout échec de vérification. Dans le .NET Framework 4.6 et 4.6.1, la méthode lève un <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> si la signature proprement dite est incorrect.|
|Suggestion|Tout code dont l’exécution dépend de la gestion du <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> doit s’exécuter à la place si la validation échoue et la méthode retourne <strong>False</strong>.|
|Portée|Mineur|
|Version|4.6.2|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Security.Cryptography.RSACng.VerifyHash(System.Byte[],System.Byte[],System.Security.Cryptography.HashAlgorithmName,System.Security.Cryptography.RSASignaturePadding)?displayProperty=nameWithType></li></ul>|

