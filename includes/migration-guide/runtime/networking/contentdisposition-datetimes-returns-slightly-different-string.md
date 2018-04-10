### <a name="contentdisposition-datetimes-returns-slightly-different-string"></a>ContentDisposition DateTimes renvoie une chaîne légèrement différente

|   |   |
|---|---|
|Détails|Représentations sous forme de chaîne de <xref:System.Net.Mime.ContentDisposition?displayProperty=name>d’ont été mis à jour, à compter de 4.6, pour toujours représenter le composant d’heure un <xref:System.DateTime?displayProperty=name> avec deux chiffres. Ce changement a pour but de se conformer aux normes [RFC822](http://www.ietf.org/rfc/rfc0822.txt) et [RFC2822](http://www.ietf.org/rfc/rfc2822.txt). <xref:System.Net.Mime.ContentDisposition.ToString> retourne à présent une chaîne légèrement différente dans la version 4.6, lorsque l’un des éléments d’heure de la disposition est antérieur à 10:00. Notez que ContentDispositions sont sérialisées parfois les convertir en chaînes, par conséquent, n’importe quel <xref:System.Net.Mime.ContentDisposition.ToString> opérations, de sérialisation ou GetHashCode appels doivent être examinées.|
|Suggestion|Ne vous attendez pas à ce que les représentations sous forme de chaîne des ContentDisposition issues de différentes versions du .NET Framework puissent être comparées correctement. Reconvertissez les chaînes en ContentDisposition, si possible, avant d’effectuer une comparaison.|
|Portée|Mineur|
|Version|4.6|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Net.Mime.ContentDisposition.ToString?displayProperty=nameWithType></li><li><xref:System.Net.Mime.ContentDisposition.GetHashCode?displayProperty=nameWithType></li></ul>|

