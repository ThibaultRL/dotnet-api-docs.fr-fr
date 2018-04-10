### <a name="wcf-msmqsecurehashalgorithm-default-value-is-now-sha256"></a>WCF MsmqSecureHashAlgorithm valeur par défaut est désormais SHA256

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.7.1, le message par défaut algorithme dans WCF pour les messages Msmq de signature est SHA256. Dans le .NET Framework 4.7 et les versions antérieures, le message d’algorithme de signature par défaut est SHA1.|
|Suggestion|Si vous rencontrez des problèmes de compatibilité avec cette modification sur le .NET Framework 4.7.1 ou une version ultérieure, vous pouvez annuler la modification en ajoutant la ligne suivante à la <code>&lt;runtime&gt;</code>section de votre fichier app.config :<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InMsmqEncryptionAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Portée|Mineur|
|Version|4.7.1|
|Type|Runtime|

