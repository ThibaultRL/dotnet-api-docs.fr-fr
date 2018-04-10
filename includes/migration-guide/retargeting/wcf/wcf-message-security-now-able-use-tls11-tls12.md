### <a name="wcf-message-security-now-is-able-to-use-tls11-and-tls12"></a>Sécurité de message WCF est désormais en mesure d’utiliser TLS 1.1 et TLS 1.2

|   |   |
|---|---|
|Détails|À compter de la 4.7 Framework .NET, clients peuvent configurer le TLS1.1 ou TLS 1.2 dans la sécurité de message WCF en plus de SSL 3.0 et TLS 1.0 via les paramètres de configuration d’application.|
|Suggestion|Dans le 4.7 .NET Framework, prise en charge de TLS 1.1 et TLS 1.2 dans la sécurité de message WCF est désactivé par défaut. Vous pouvez l’activer en ajoutant la ligne suivante à la <code>&lt;runtime&gt;</code> section du fichier app.config ou web.config :<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableUsingServicePointManagerSecurityProtocols=false;Switch.System.Net.DontEnableSchUseStrongCrypto=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.7|
|Type|Reciblage|

