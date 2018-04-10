### <a name="adonet-now-attempts-to-automatically-reconnect-broken-sql-connections"></a>ADO.NET maintenant tente de se reconnecter automatiquement les connexions SQL rompues

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.5.1, le .NET Framework tente de se reconnecter automatiquement les connexions SQL interrompues. Bien que cela effectue généralement des applications plus fiables, il existe des cas dans lesquels une application a besoin de savoir que la connexion a été perdue afin qu’il peut intervenir lors de la reconnexion.|
|Suggestion|Si cette fonctionnalité n’est pas souhaitable pour des raisons de compatibilité, il peut être désactivé en définissant le <xref:System.Data.SqlClient.SqlConnectionStringBuilder.ConnectRetryCount?displayProperty=name> propriété de chaîne de connexion (ou <xref:System.Data.SqlClient.SqlConnectionStringBuilder?displayProperty=name>) à 0.|
|Portée|Microsoft Edge|
|Version|4.5.1|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Data.IDbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Configuration.ConnectionStringSettings.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor(System.Boolean)?displayProperty=nameWithType></li></ul>|

