### <a name="servicebase-doesnt-propagate-onstart-exceptions"></a>ServiceBase ne propage les exceptions OnStart

|   |   |
|---|---|
|Détails|Dans le .NET Framework 4.7 et les versions antérieures, les exceptions levées au démarrage du service ne sont pas propagées à l’appelant de <xref:System.ServiceProcess.ServiceBase.Run%2A?displayProperty=nameWithType>. Compter les applications qui ciblent le .NET Framework 4.7.1, le runtime propage les exceptions à <xref:System.ServiceProcess.ServiceBase.Run%2A?displayProperty=nameWithType> pour les services qui ne parviennent pas à démarrer.|
|Suggestion|Sur le démarrage du service, s’il existe une exception, cette exception est propagée. Cela doit aider à diagnostiquer les cas où les services démarreront pas. Si ce comportement est indésirable, vous pouvez refuser en ajoutant le code suivant <AppContextSwitchOverrides> élément à la <runtime> section du fichier de configuration de votre application :<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceProcess.DontThrowExceptionsOnStart=true&quot; /&gt;&#13;&#10;</code></pre>Si votre application cible une version antérieure à 4.7.1 mais que vous souhaitez que ce problème, ajoutez le code suivant <AppContextSwitchOverrides> élément à la <runtime> section du fichier de configuration de votre application :<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceProcess.DontThrowExceptionsOnStart=false&quot; /&gt;&#13;&#10;</code></pre>|
|Portée|Mineur|
|Version|4.7.1|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.ServiceProcess.ServiceBase.Run(System.ServiceProcess.ServiceBase)?displayProperty=nameWithType></li><li><xref:System.ServiceProcess.ServiceBase.Run(System.ServiceProcess.ServiceBase[])?displayProperty=nameWithType></li></ul>|

