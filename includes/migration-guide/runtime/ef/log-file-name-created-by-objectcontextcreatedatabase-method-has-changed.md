### <a name="log-file-name-created-by-the-objectcontextcreatedatabase-method-has-changed-to-match-sql-server-specifications"></a>Nom du fichier journal créé par la méthode ObjectContext.CreateDatabase a changé en fonction des spécifications de SQL Server

|   |   |
|---|---|
|Détails|Lorsque la <xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=name> méthode est appelée directement ou à l’aide de Code First avec le fournisseur SqlClient et une valeur de AttachDBFilename dans la chaîne de connexion, il crée un fichier journal nommé filename_log.ldf au lieu de filename.ldf (où filename est le nom de le fichier spécifié par la valeur de AttachDBFilename). Cette modification améliore le débogage en fournissant un fichier journal dont le nom répond aux spécifications SQL Server.|
|Suggestion|Si le nom du fichier journal est important pour une application, celle-ci doit être mise à jour pour attendre le format de nom de fichier standard « _log.ldf ».|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=nameWithType></li></ul>|

