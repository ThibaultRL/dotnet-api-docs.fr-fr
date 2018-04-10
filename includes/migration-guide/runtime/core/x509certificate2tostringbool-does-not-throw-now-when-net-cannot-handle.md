### <a name="x509certificate2tostringbool-does-not-throw-now-when-net-cannot-handle-the-certificate"></a>X509Certificate2.ToString(bool) ne lève pas maintenant lorsque .NET ne peut pas gérer le certificat

|   |   |
|---|---|
|Détails|Auparavant, cette méthode lève si <code>true</code> a été transmise pour le paramètre verbose et a installé les certificats qui n’ont pas été pris en charge par le .NET Framework. À présent, la méthode réussissent et retourner une chaîne valide qui omet les parties inaccessibles du certificat.|
|Suggestion|Tout code selon <xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)> doivent être mis à jour pour attendre que la chaîne retournée peut exclure certaines données de certificat (telles que la clé publique, clé privée et extensions) dans certains cas dans lequel l’API aurait précédemment levée.|
|Portée|Microsoft Edge|
|Version|4.6|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)?displayProperty=nameWithType></li></ul>|

