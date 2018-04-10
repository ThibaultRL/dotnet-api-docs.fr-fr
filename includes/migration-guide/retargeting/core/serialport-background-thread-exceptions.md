### <a name="serialport-background-thread-exceptions"></a>Exceptions de thread d’arrière-plan SerialPort

|   |   |
|---|---|
|Détails|Créé avec des threads d’arrière-plan <xref:System.IO.Ports.SerialPort> flux n’est plus le processus de fin lors de la levée des exceptions de système d’exploitation. Dans les applications qui ciblent le .NET Framework 4.7 et les versions antérieures, un processus est terminé en cas d’exception de système d’exploitation sur un thread d’arrière-plan créé avec un <xref:System.IO.Ports.SerialPort> flux. Dans les applications que cible le .NET Framework 4.7.1 ou une version ultérieure, les threads d’arrière-plan attend la fin des événements du système d’exploitation liés au port série actif et peut se bloquer dans certains cas, comme la suppression soudaine du port série.|
|Suggestion|Pour les applications qui ciblent le .NET Framework 4.7.1, vous pouvez désactiver la gestion des exceptions si elle n’est pas souhaitable en ajoutant le code suivant à la <code>&lt;runtime&gt;</code> section de votre <code>app.config</code> fichier :<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Pour les applications qui ciblent des versions antérieures du .NET Framework mais exécutent sur le .NET Framework 4.7.1 ou une version ultérieure, vous pouvez participer à l’exception de gestion en ajoutant le code suivant à la <code>&lt;runtime&gt;</code> section de votre <code>app.config</code> fichier :<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Portée|Mineur|
|Version|4.7.1|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.IO.Ports.SerialPort?displayProperty=nameWithType></li></ul>|

