### <a name="icontobitmap-successfully-converts-icons-with-png-frames-into-bitmap-objects"></a>Icon.ToBitmap convertit correctement les icônes dotées de cadres PNG en objets Bitmap

|   |   |
|---|---|
|Détails|En commençant par les applications qui ciblent le .NET Framework 4.6, la <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> méthode convertit correctement les icônes dotées de cadres PNG en objets de l’image Bitmap. Dans les applications qui ciblent le .NET Framework 4.5.2 et versions antérieures, le <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> méthode lève une exception une <xref:System.ArgumentOutOfRangeException> exception si l’objet d’icône comporte des cadres PNG. Cette modification affecte les applications qui sont recompilées pour cibler le .NET Framework 4.6 et qui implémentent un traitement spécial pour la <xref:System.ArgumentOutOfRangeException> qui est levée lorsqu’un objet d’icône comporte des cadres PNG. Dans le cadre d’une exécution sous le .NET Framework 4.6, la conversion aboutit, il n’est plus levé d’exception <xref:System.ArgumentOutOfRangeException> et, de ce fait, le gestionnaire d’exceptions n’est plus appelé.|
|Suggestion|Si ce comportement est indésirable, vous pouvez conserver le comportement antérieur en ajoutant l’élément suivant à la <code>&lt;runtime&gt;</code> section de votre fichier app.config :<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true&quot; /&gt;&#13;&#10;</code></pre>Si le fichier app.config contient déjà le <code>AppContextSwitchOverrides</code> élément, la nouvelle valeur doit être fusionnée avec l’attribut de valeur comme suit :<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true;&lt;previous key&gt;=&lt;previous value&gt;&quot; /&gt;&#13;&#10;</code></pre>|
|Portée|Mineur|
|Version|4.6|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Drawing.Icon.ToBitmap?displayProperty=nameWithType></li></ul>|

