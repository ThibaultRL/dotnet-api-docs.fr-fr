### <a name="deadlock-may-result-when-using-reentrant-services"></a>Blocage peut entraîner lors de l’utilisation des services réentrants

|   |   |
|---|---|
|Détails|Un service réentrant, ce qui restreint les instances du service à un thread d’exécution à la fois peut entraîner un blocage. Services susceptible de rencontrer ce problème aura suit <xref:System.ServiceModel.ServiceBehaviorAttribute> dans leur code :<pre><code class="language-csharp">[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Reentrant)]&#13;&#10;</code></pre>|
|Suggestion|Pour résoudre ce problème, vous pouvez procédez comme suit :<ul><li>Définir le mode du service d’accès concurrentiel <xref:System.ServiceModel.ConcurrencyMode.Single?displayProperty=nameWithType> ou &lt;System.ServiceModel.ConcurrencyMode.Multiple?displayProperty=nameWithType&gt;. Exemple :</li></ul><pre><code class="language-csharp">[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Single)]&#13;&#10;</code></pre><ul><li>Installez la dernière mise à jour du Kit de développement .NET Framework 4.6.2 ou mettre à niveau vers une version ultérieure du .NET Framework. Cela désactive le flux de la <xref:System.Threading.ExecutionContext> dans <xref:System.ServiceModel.OperationContext.Current?displayProperty=nameWithType>. Ce comportement est configurable ; Il est équivalent à l’ajout du paramètre d’application suivant à votre fichier de configuration :</li></ul><pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;Switch.System.ServiceModel.DisableOperationContextAsyncFlow&quot; value=&quot;true&quot; /&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;&#13;&#10;The value of &#39;Switch.System.ServiceModel.DisableOperationContextAsyncFlow&#39; should never be set to &#39;false&#39; for Rentrant services.&#13;&#10;</code></pre>|
|Portée|Mineur|
|Version|4.6.2|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.ServiceModel.ServiceBehaviorAttribute?displayProperty=nameWithType></li><li><xref:System.ServiceModel.ConcurrencyMode.Reentrant?displayProperty=nameWithType></li></ul>|

