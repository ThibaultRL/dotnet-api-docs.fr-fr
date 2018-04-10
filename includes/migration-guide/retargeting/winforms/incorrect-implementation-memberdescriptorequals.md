### <a name="incorrect-implementation-of-memberdescriptorequals"></a>Implémentation incorrecte de MemberDescriptor.Equals

|   |   |
|---|---|
|Détails|Implémentation d’origine de &quot;est égal à&quot; méthode a été comparant deux propriétés de chaîne différents à partir des objets sous comparaison : nom de catégorie pour la chaîne de description. La solution consiste à comparer &quot;catégorie&quot; du premier objet à &quot;catégorie&quot; de la seconde et &quot;description&quot; à &quot;description&quot;. Valeur de configuration de MemberDescriptorEqualsReturnsFalseIfEquivalent peut être définie sur true pour désactiver le nouveau comportement si 4.6.2 ou false pour activer ce correctif lorsque cibler la version de framework est inférieur à 4.6.2.|
|Suggestion|Si votre application dépend de MemberDescriptor.Equals parfois retournant la valeur false lorsque les descripteurs sont équivalents, et que vous prévoyez 4.6.2 version du .NET Framework, vous disposez de plusieurs options :<ol><li>Apporter des modifications de code à comparer &quot;catégorie&quot; et &quot;description&quot; champs manuellement en plus de la méthode Equals en cours d’exécution.</li><li>Choisir à partir de cette modification en ajoutant la valeur suivante au fichier app.config :</li></ol><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Si votre application cible 4.6.1 ou une version antérieure de .NET Framework et que vous souhaitez que cette modification activée, vous pouvez définir le commutateur de compatibilité à false en ajoutant la valeur suivante au fichier app.config :<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.6.2|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.ComponentModel.MemberDescriptor.Equals(System.Object)?displayProperty=nameWithType></li></ul>|

