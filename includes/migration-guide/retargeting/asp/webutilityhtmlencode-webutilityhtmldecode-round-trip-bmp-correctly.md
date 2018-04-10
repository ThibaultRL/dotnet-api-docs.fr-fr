### <a name="webutilityhtmlencode-and-webutilityhtmldecode-round-trip-bmp-correctly"></a>WebUtility.HtmlEncode et BMP aller-retour de WebUtility.HtmlDecode correctement

|   |   |
|---|---|
|Détails|Pour les applications qui ciblent le .NET Framework 4.5, les caractères situés en dehors de l’aller-retour base plan BMP (Multilingual Plane) correctement lorsqu’ils sont passés à la <xref:System.Net.WebUtility.HtmlDecode(System.String)> méthodes.|
|Suggestion|Cette modification doit n’ont aucun effet sur les applications actuelles, mais pour restaurer le comportement d’origine, vous devez définir le <code>targetFramework</code> attribut de la <code>&lt;httpRuntime&gt;</code> élément à une chaîne autre que &quot;4.5&quot;. Vous pouvez également définir les attributs <code>unicodeEncodingConformance</code> et <code>unicodeDecodingConformance</code> de l'élément de configuration <code>&lt;webUtility&gt;</code> pour contrôler ce comportement indépendamment de la version ciblée du .NET Framework.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Net.WebUtility.HtmlEncode(System.String)?displayProperty=nameWithType></li><li><xref:System.Net.WebUtility.HtmlEncode(System.String,System.IO.TextWriter)?displayProperty=nameWithType></li></ul>|

