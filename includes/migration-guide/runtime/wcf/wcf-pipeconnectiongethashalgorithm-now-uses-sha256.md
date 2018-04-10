### <a name="wcf-pipeconnectiongethashalgorithm-now-uses-sha256"></a>WCF PipeConnection.GetHashAlgorithm utilise désormais SHA256

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.7.1, Windows Communication Foundation utilise un hachage SHA256 pour générer des noms aléatoires pour les canaux nommés. Dans le .NET Framework 4.7 et les versions antérieures, il utilisé par le hachage SHA1.|
|Suggestion|Si vous rencontrez des problème de compatibilité avec cette modification sur le .NET Framework 4.7.1 ou une version ultérieure, vous pouvez annuler il en ajoutant la ligne suivante à la <code>&lt;runtime&gt;</code> section de votre fichier app.config :<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InPipeConnectionGetHashAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Portée|Mineur|
|Version|4.7.1|
|Type|Runtime|

