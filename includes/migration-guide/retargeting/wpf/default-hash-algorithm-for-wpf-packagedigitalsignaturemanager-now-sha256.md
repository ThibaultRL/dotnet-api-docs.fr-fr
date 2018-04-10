### <a name="the-default-hash-algorithm-for-wpf-packagedigitalsignaturemanager-is-now-sha256"></a>L’algorithme de hachage par défaut pour WPF PackageDigitalSignatureManager est désormais SHA256

|   |   |
|---|---|
|Détails|Le <code>System.IO.Packaging.PackageDigitalSignatureManager</code> fournit les fonctionnalités pour les signatures numériques en relation avec les packages WPF.  Dans le .NET Framework 4.7 et versions antérieures, l’algorithme par défaut (<xref:System.IO.Packaging.PackageDigitalSignatureManager.DefaultHashAlgorithm?displayProperty=nameWithType>) utilisé pour la signature des parties d’un package a été SHA1.  En raison des récents problèmes de sécurité avec SHA1, cette valeur par défaut a été remplacé par SHA256 en commençant par le .NET Framework 4.7.1.  Cette modification affecte toutes les signature du package, y compris les documents XPS.|
|Suggestion|Un développeur qui souhaite utiliser cette modification pendant le ciblage d’une version de framework ci-dessous .NET 4.7.1 ou un développeur qui nécessite des fonctionnalités précédentes lors de la détermination .NET 4.7.1 ou supérieur peuvent définie l’indicateur AppContext suivant en conséquence.  La valeur true entraîne SHA1 utilisé en tant que l’algorithme par défaut ; / / donne false SHA256.<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.UseSha1AsDefaultHashAlgorithmForDigitalSignatures=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.7.1|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.IO.Packaging.PackageDigitalSignatureManager.DefaultHashAlgorithm?displayProperty=nameWithType></li></ul>|

