### <a name="signedxmlgetpublickey-returns-rsacng-on-net462-or-lightup-without-retargeting-change"></a>SignedXml.GetPublicKey retourne RSACng sur net462 (ou lightup) sans modification de reciblage

|   |   |
|---|---|
|Détails|En commençant par le .NET Framework 4.6.2, le type concret de l’objet retourné par la <xref:System.Security.Cryptography.Xml.SignedXml.GetPublicKey%2A?displayProperty=nameWithType> méthode modifiée (sans une particularité) à partir d’une implémentation CryptoServiceProvider vers une implémentation Cng. Il s’agit, car il est modifié par l’implémentation de l’utilisation <code>certificate.PublicKey.Key</code> à l’utilisation interne <code>certificate.GetAnyPublicKey</code> qui transfère à <xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey%2A?displayProperty=nameWithType>.|
|Suggestion|Compter des applications en cours d’exécution sur le .NET Framework 4.7.1, vous pouvez utiliser l’implémentation CryptoServiceProvider utilisée par défaut dans le .NET Framework 4.6.1 et versions antérieures en ajoutant la configuration suivante basculer vers le [runtime](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)section de votre fichier de configuration d’application :<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.SignedXmlUseLegacyCertificatePrivateKey=true&quot; /&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.6.2|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Security.Cryptography.Xml.SignedXml.CheckSignatureReturningKey(System.Security.Cryptography.AsymmetricAlgorithm@)?displayProperty=nameWithType></li></ul>|

