### <a name="wf-serializes-expressionsliterallttgt-datetimes-differently-now-breaks-custom-xaml-parsers"></a>WF sérialise Expressions.Literal&lt;T&gt; dates/heures différemment maintenant (sauts analyseurs XAML personnalisés)

|   |   |
|---|---|
|Détails|Associé <xref:System.Windows.Markup.ValueSerializer> objet convertit un <xref:System.DateTime?displayProperty=name> ou <xref:System.DateTimeOffset?displayProperty=name> dont l’objet ensuite et <xref:System.DateTime.Millisecond?displayProperty=name> composants sont différente de zéro et (pour un <xref:System.DateTime?displayProperty=name> valeur) dont <xref:System.DateTime.Kind> propriété n’est pas non spécifiée pour l’élément de propriété syntaxe à la place d’une chaîne. Cette modification permet aux valeurs <xref:System.DateTime?displayProperty=name> et <xref:System.DateTimeOffset?displayProperty=name> de faire l'objet d'un aller-retour. Les analyseurs XAML personnalisés qui supposent que l'entrée XAML figure dans la syntaxe d'attribut ne fonctionnent pas correctement.|
|Suggestion|Cette modification permet aux valeurs <xref:System.DateTime?displayProperty=name> et <xref:System.DateTimeOffset?displayProperty=name> de faire l'objet d'un aller-retour. Les analyseurs XAML personnalisés qui supposent que l'entrée XAML figure dans la syntaxe d'attribut ne fonctionnent pas correctement.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|

