### <a name="multi-line-aspnet-textbox-spacing-changed-when-using-antixssencoder"></a>Espacement d’ASP.Net de zone de texte multiligne modifiée lorsque vous utilisez AntiXSSEncoder

|   |   |
|---|---|
|Détails|Dans le .NET Framework 4.0, des lignes supplémentaires étaient insérées dans la zone de texte multiligne lors de la publication (postback), quand vous utilisiez <xref:System.Web.Security.AntiXss.AntiXssEncoder?displayProperty=name>. Dans le .NET Framework 4.5, ces sauts de ligne supplémentaires ne sont pas inclus si l’application web cible .NET 4.5.|
|Suggestion|Notez que les applications web 4.0 reciblées vers .NET 4.5 peuvent avoir des zones de texte multilignes améliorées qui ne comportent plus de sauts de ligne supplémentaires. Si ce n’est pas souhaitable, l’application peut avoir l’ancien comportement lors de l’exécution sur le .NET Framework 4.5 en ciblant le .NET Framework 4.0.|
|Portée|Mineur|
|Version|4.5|
|Type|Reciblage|

