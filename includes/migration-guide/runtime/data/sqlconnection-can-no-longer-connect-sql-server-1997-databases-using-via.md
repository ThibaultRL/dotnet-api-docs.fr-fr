### <a name="sqlconnection-can-no-longer-connect-to-sql-server-1997-or-databases-using-the-via-adapter"></a>SqlConnection peut ne plus se connecter à SQL Server 1997 ou des bases de données à l’aide de l’adaptateur VIA

|   |   |
|---|---|
|Détails|Connexions aux bases de données SQL Server à l’aide de la [adaptateur VIA (Virtual Interface) protocole](https://technet.microsoft.com/library/ms191229%28v=sql.105%29.aspx) ne sont plus prises en charge. Le protocole utilisé pour se connecter à une base de données SQL Server est visible dans la chaîne de connexion. Une connexion VIA contiendra :&lt;nom_serveur&gt;. Si cette application se connecte à SQL via un autre protocole que le protocole VIA (tcp : ou np : par exemple), alors aucune modification avec rupture n’est détectée. En outre, les connexions à SQL Server 7 (1997) ne sont plus prises en charge.|
|Suggestion|Le protocole VIA est déconseillé, donc un autre protocole doit être utilisé pour se connecter aux bases de données SQL. Protocole le plus utilisé est TCP/IP. Instructions pour l’activation du protocole TCP/IP sont accessibles [ici](https://msdn.microsoft.com/library/bb909712.aspx). Si la base de données est accessible uniquement à partir d’un intranet, le protocole des canaux partagé peut offrir de meilleures performances si le réseau est lent.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String,System.Data.SqlClient.SqlCredential)?displayProperty=nameWithType></li></ul>|

