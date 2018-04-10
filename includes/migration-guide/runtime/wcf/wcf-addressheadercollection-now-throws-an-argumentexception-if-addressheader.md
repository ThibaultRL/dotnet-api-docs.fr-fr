### <a name="wcf-addressheadercollection-now-throws-an-argumentexception-if-an-addressheader-element-is-null"></a>Collection AddressHeaderCollection de WCF présent lève une exception ArgumentException si un élément addressHeader est null

|   |   |
|---|---|
|Détails|En commençant par le .NET Framework 4.7.1, le <xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})> constructeur lève une <xref:System.ArgumentException> si un des éléments est <code>null</code>. Dans le .NET Framework 4.7 et les versions antérieures, aucune exception n’est levée.|
|Suggestion|Si vous rencontrez des problèmes de compatibilité avec cette modification sur le .NET Framework 4.7.1 ou une version ultérieure, vous pouvez annuler de celui-ci en ajoutant la ligne suivante à la <code>&lt;runtime&gt;</code> section du fichier app.config :<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableAddressHeaderCollectionValidation=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Portée|Mineur|
|Version|4.7.1|
|Type|Runtime|
|API affectées|<ul><li><xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})?displayProperty=nameWithType></li></ul>|

