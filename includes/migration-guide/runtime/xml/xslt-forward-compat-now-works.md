### <a name="xslt-forward-compat-now-works"></a>Compatibilité ascendante de XSLT fonctionne maintenant

|   |   |
|---|---|
|Détails|Dans le .NET Framework 4, la compatibilité ascendante XSLT 1.0 présentait les problèmes suivants :<ul><li>Le chargement d'une feuille de style échouait si sa version avait la valeur 2.0 et si l'analyseur rencontrait une construction XSLT 1.0 non reconnue.</li><li>La construction <code>xsl:sort</code> ne pouvait pas trier les données si la version de la feuille de style était définie sur 1.1.</li></ul>Dans le .NET Framework 4.5, ces problèmes ont été résolus, et le mode de compatibilité ascendante XSLT 1.0 fonctionne correctement.|
|Suggestion|La plupart des applications doit être pas affectées, mais les données seront triées différemment dans certains cas maintenant que xsl : sort est respectée. Si <code>xsl:sort</code> est utilisé dans les feuilles de style 1.1, vérifiez que les applications ont été pas selon l’ordre avec des données. Si les applications s’appuient sur le comportement de tri de 4.0, supprimez <code>xsl:sort</code> à partir de la feuille de style.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Xml.Xsl.XslCompiledTransform?displayProperty=nameWithType></li></ul>|

