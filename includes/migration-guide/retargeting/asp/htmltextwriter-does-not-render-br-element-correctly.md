### <a name="htmltextwriter-does-not-render-br-element-correctly"></a>HtmlTextWriter n’est pas rendu `<br/>` élément correctement

|   |   |
|---|---|
|Détails|À compter de la version 4.6 du .NET Framework, l’appel de <xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)> et <xref:System.Web.UI.HtmlTextWriter.RenderEndTag> avec un élément <code>&lt;BR /&gt;</code> aboutit à l’insertion d’un seul <code>&lt;BR /&gt;</code> (au lieu de deux).|
|Suggestion|Si une application dépendait de la balise <code>&lt;BR /&gt;</code> supplémentaire, <xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)> doit être appelé une deuxième fois. Notez que cette modification affecte uniquement les applications qui ciblent le .NET Framework 4.6 ou version ultérieur, une autre option consiste donc à cibler une version antérieure du .NET Framework afin d’obtenir l’ancien comportement.|
|Portée|Microsoft Edge|
|Version|4.6|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)?displayProperty=nameWithType></li><li><xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.Web.UI.HtmlTextWriterTag)?displayProperty=nameWithType></li></ul>|

