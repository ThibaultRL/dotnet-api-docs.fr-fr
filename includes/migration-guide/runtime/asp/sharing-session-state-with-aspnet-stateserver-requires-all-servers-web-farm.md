### <a name="sharing-session-state-with-aspnet-stateserver-requires-all-servers-in-the-web-farm-to-use-the-same-net-framework-version"></a>Partager l’état de session avec Asp.Net StateServer nécessite tous les serveurs de la batterie de serveurs web à utiliser la même version de .NET Framework

|   |   |
|---|---|
|Détails|Lors de l’activation <xref:System.Web.SessionState.SessionStateMode.StateServer?displayProperty=name> d’état de session, tous les serveurs dans la batterie de serveurs web donné doivent utiliser la même version du .NET Framework par ordre d’état à être partagé correctement.|
|Suggestion|Veillez à mettre à niveau les versions du .NET Framework sur les serveurs web qui partagent l’état en même temps.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Web.SessionState.SessionStateMode.StateServer?displayProperty=nameWithType></li></ul>|

