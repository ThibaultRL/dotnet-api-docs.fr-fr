### <a name="gridviews-with-allowcustompaging-set-to-true-may-fire-the-pageindexchanging-event-when-leaving-the-final-page-of-the-view"></a>Contrôles GridView avec la valeur true AllowCustomPaging peut déclencher l’événement de PageIndexChanging quand vous quittez la page finale de la vue

|   |   |
|---|---|
|Détails|Un bogue dans le .NET Framework 4.5 <xref:System.Web.UI.WebControls.GridView.PageIndexChanging?displayProperty=name> parfois non-déclenchement pour <xref:System.Web.UI.WebControls.GridView?displayProperty=name>s qui ont activé <xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=name>.|
|Suggestion|Ce problème a été résolu dans le .NET Framework 4.6 et peut être adressé par la mise à niveau vers cette version du .NET Framework. Comme une solution de contournement, l’application peut faire un BindGrid explicite sur n’importe quel <code>Page_Load</code> qui atteint ces conditions (le <xref:System.Web.UI.WebControls.GridView?displayProperty=name> est dans la page et le dernier dernière<xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name> est différente de <xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name>). Vous pouvez également l’application sont modifiables pour autoriser la pagination (au lieu de la pagination personnalisée), comme ce scénario ne présente pas le problème.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=nameWithType></li></ul>|

