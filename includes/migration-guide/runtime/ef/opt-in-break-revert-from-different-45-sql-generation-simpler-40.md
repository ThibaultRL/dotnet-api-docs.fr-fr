### <a name="opt-in-break-to-revert-from-different-45-sql-generation-to-simpler-40-sql-generation"></a>Acceptation de saut de rétablir la génération SQL 4.5 différents 4.0 plus simple de la génération SQL

|   |   |
|---|---|
|Détails|Les requêtes qui produisent des instructions de jointure et contient un appel à une opération de limitation sans d’abord à l’aide de OrderBy maintenant produisent un langage SQL plus simple. Après la mise à niveau vers .NET Framework 4.5, ces requêtes produisent un langage SQL plus compliqué que les versions antérieures.|
|Suggestion|Cette fonctionnalité est désactivée par défaut. Si Entity Framework génère des instructions de jointure supplémentaires qui entraînent une dégradation des performances, vous pouvez activer cette fonctionnalité en ajoutant l’entrée suivante à la <code>&lt;appSettings&gt;</code> section du fichier de configuration (app.config) d’application :<pre><code class="language-xml">&lt;add key=&quot;EntityFramework_SimplifyLimitOperations&quot; value=&quot;true&quot; /&gt;&#13;&#10;</code></pre>|
|Portée|Transparent|
|Version|4.5.2|
|Type|Runtime|

