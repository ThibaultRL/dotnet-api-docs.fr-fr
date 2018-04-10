### <a name="calling-createdefaultauthorizationcontext-with-a-null-argument-has-changed"></a>Appel de CreateDefaultAuthorizationContext avec un argument null a été modifié

|   |   |
|---|---|
|Détails|L’implémentation de la <xref:System.IdentityModel.Policy.AuthorizationContext?displayProperty=name> retourné par un appel à la <xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext(System.Collections.Generic.IList{System.IdentityModel.Policy.IAuthorizationPolicy})?displayProperty=name> avec une valeur null authorizationPolicies argument a changé dans le .NET Framework 4.6.|
|Suggestion|Dans de rares cas, les applications WCF qui utilisent l'authentification personnalisée peuvent voir les différences de comportement. Dans ce cas, vous pouvez restaurer l’ancien comportement de deux manières :<ol><li>Recompiler l'application pour cibler une version antérieure du .NET Framework autre que 4.6. Pour les services hébergés dans IIS, utilisez le &lt;httpRuntime targetFramework =&quot;x.x&quot;  / &gt; élément à cibler une version antérieure du .NET Framework.</li><li>Ajoutez la ligne suivante à la section <code>&lt;appSettings&gt;</code> de votre fichier app.config : <code>&lt;add key=&quot;appContext.SetSwitch:Switch.System.IdentityModel.EnableCachedEmptyDefaultAuthorizationContext&quot; value=&quot;true&quot; /&gt;</code></li></ol>|
|Portée|Mineur|
|Version|4.6|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext(System.Collections.Generic.IList{System.IdentityModel.Policy.IAuthorizationPolicy})?displayProperty=nameWithType></li></ul>|

