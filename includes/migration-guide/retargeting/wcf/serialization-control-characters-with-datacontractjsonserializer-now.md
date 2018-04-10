### <a name="serialization-of-control-characters-with-datacontractjsonserializer-is-now-compatible-with-ecmascript-v6-and-v8"></a>Sérialisation de caractères de contrôle avec DataContractJsonSerializer est désormais compatible avec ECMAScript V6 et V8

|   |   |
|---|---|
|Détails|Dans le .NET framework 4.6.2 et les versions antérieures, le <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=name> ne pas sérialiser certains caractères de contrôle spéciales, telles que \b, \f et \t, d’une manière qui est compatible avec les normes ECMAScript V6 et V8. À compter de la 4.7 Framework .NET, la sérialisation de ces caractères de contrôle est compatible avec ECMAScript V6 et V8.|
|Suggestion|Pour les applications qui ciblent le 4.7 Framework .NET, cette fonctionnalité est activée par défaut. Si ce comportement n’est pas souhaitable, vous pouvez désactiver cette fonctionnalité en ajoutant la ligne suivante à la section <code>&lt;runtime&gt;</code> du fichier app.config ou au fichier web.config :<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Runtime.Serialization.DoNotUseECMAScriptV6EscapeControlCharacter=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.7|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlDictionaryWriter,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlWriter,System.Object)?displayProperty=nameWithType></li></ul>|

