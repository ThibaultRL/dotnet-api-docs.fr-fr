### <a name="ef-no-longer-throws-for-queryviews-with-specific-characteristics"></a>EF ne lève plus pour QueryView avec des caractéristiques spécifiques

|   |   |
|---|---|
|Détails|Entity Framework ne lève plus une <xref:System.StackOverflowException?displayProperty=name> exception quand une application exécute une requête qui implique un QueryView avec une valeur 0.. 1 propriété de navigation qui tente d’inclure les entités associées dans le cadre de la requête. Par exemple, en appelant <code>.Include(e =&gt; e.RelatedNavProp)</code>.|
|Suggestion|Cette modification affecte uniquement le code qui utilise des QueryView avec 1-valeur 0.. 1 pour exécuter des requêtes qui appellent des relations. Inclure. Elle permet d'améliorer la fiabilité et doit être transparente pour presque toutes les applications. Toutefois, si elle entraîne un comportement inattendu, vous pouvez la désactiver en ajoutant l'entrée suivante à la section <code>&lt;appSettings&gt;</code> du fichier de configuration de l'application :<pre><code class="language-xml">&lt;add key=&quot;EntityFramework_SimplifyUserSpecifiedViews&quot; value=&quot;false&quot; /&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.5.2|
|Type|Runtime|

