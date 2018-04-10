### <a name="wcf-binding-with-the-transportwithmessagecredential-security-mode"></a>Liaison WCF avec le mode de sécurité TransportWithMessageCredential

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.6.1, une liaison WCF qui utilise le mode de sécurité TransportWithMessageCredential peut être configurée pour recevoir des messages avec non signé &quot;à&quot; en-têtes pour les clés de sécurité asymétrique. Par défaut, non signé &quot;à&quot; en-têtes continueront à être rejeté dans .NET 4.6.1. Ils seront acceptées uniquement si une application opte pour ce nouveau mode d’opération en utilisant le commutateur de configuration Switch.System.ServiceModel.AllowUnsignedToHeader. Car il s’agit d’une fonctionnalité d’abonnement, il ne doit pas affectent le comportement des applications existantes.|
|Suggestion|Parce qu’il s’agit d’une fonctionnalité d’abonnement, le comportement des applications existantes ne devrait pas être affecté. Pour contrôler si le nouveau comportement est utilisé ou non, utilisez le paramètre de configuration suivantes :<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.AllowUnsignedToHeader=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Portée|Transparent|
|Version|4.6.1|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.ServiceModel.BasicHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.BasicHttpsSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.WSFederationHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li></ul>|

