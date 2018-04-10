### <a name="throttle-concurrent-requests-per-session"></a>Restriction des demandes simultanées par session

|   |   |
|---|---|
|Détails|Dans le .NET Framework 4.6.2 précédemment, ASP.NET exécute séquentiellement des demandes avec le même ID de session et ASP.NET émet toujours l’ID de session via les cookies par défaut. Si une page prend beaucoup de temps pour répondre, il sera nuire considérablement aux performances du serveur simplement en appuyant sur F5 dans le navigateur. Le correctif, nous avons ajouté un compteur permettant de suivre les demandes en file d’attente et les requêtes de fermeture lorsqu’elles dépassent la limite spécifiée. La valeur par défaut est 50. Si la limite est atteinte, un avertissement sera consigné dans le journal et une réponse HTTP 500 doivent être enregistrées dans le journal IIS des événements.|
|Suggestion|Pour restaurer l’ancien comportement, vous pouvez ajouter le paramètre suivant à votre fichier web.config pour désactiver le nouveau comportement.<pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;aspnet:RequestQueueLimitPerSession&quot; value=&quot;2147483647&quot;/&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.7|
|Type|Reciblage|

