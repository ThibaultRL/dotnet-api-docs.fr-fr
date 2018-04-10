### <a name="attempting-a-tcpip-connection-to-a-sql-server-database-that-resolves-to-localhost-fails"></a>Une tentative de connexion à une base de données SQL Server qui correspond à TCP/IP `localhost` échoue

|   |   |
|---|---|
|Détails|Dans le .NET Framework 4.6 et 4.6.1, une tentative de connexion TCP/IP à une base de données SQL Server qui se résout en <code>localhost</code> échoue avec l’erreur, &quot;une erreur liée au réseau ou d’instance spécifique s’est produite lors de l’établissement d’une connexion à SQL Server. Le serveur est introuvable ou n’est pas accessible. Vérifiez que le nom de l’instance est correct et que SQL Server est configuré pour autoriser les connexions distantes. (fournisseur : Interfaces réseau SQL, erreur : 26 - erreur serveur/de l’Instance spécifiée de localisation)&quot;|
|Suggestion|Ce problème a été résolu et le comportement précédent est restauré dans le .NET Framework 4.6.2. Pour vous connecter à un Microsoft Azure SQL Server qui se résout en <code>localhost</code>, mise à niveau vers le Kit de développement .NET Framework 4.6.2.|
|Portée|Mineur|
|Version|4.6|
|Type|Runtime|

