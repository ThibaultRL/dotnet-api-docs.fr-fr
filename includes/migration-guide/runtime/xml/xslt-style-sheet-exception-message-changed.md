### <a name="xslt-style-sheet-exception-message-changed"></a>Messages d’exception de feuille de style XSLT modifié

|   |   |
|---|---|
|Détails|Dans le .NET Framework 4.5, le texte du message d’erreur lorsqu’un fichier XSLT est trop complexe est &quot;la feuille de style est trop complexe.&quot; Dans les versions précédentes, le message d’erreur a été &quot;erreur de compilation XSLT.&quot; Le code d'application qui dépend du texte du message d'erreur ne fonctionne plus. Toutefois, comme les types d’exception restent les mêmes, cette modification ne devrait pas avoir d’impact réel.|
|Suggestion|Mettre à jour de n’importe quel code d’application, selon le message d’exception à partir de cette condition d’erreur pour attendre le nouveau message, ou (mieux) mettre à jour le code de façon à dépendre uniquement le type d’exception (<xref:System.Xml.Xsl.XsltException?displayProperty=name>), qui n’a pas changé.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Type)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XmlReader)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XPath.IXPathNavigable)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Reflection.MethodInfo,System.Byte[],System.Type[])?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.String,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XmlReader,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XPath.IXPathNavigable,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li></ul>|

