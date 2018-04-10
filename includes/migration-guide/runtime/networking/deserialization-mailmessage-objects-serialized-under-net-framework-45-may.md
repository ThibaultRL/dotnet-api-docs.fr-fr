### <a name="deserialization-of-mailmessage-objects-serialized-under-the-net-framework-45-may-fail"></a>La désérialisation des objets MailMessage sérialisés sous le .NET Framework 4.5 peut échouer.

|   |   |
|---|---|
|Détails|En commençant par le .NET Framework 4.5, <xref:System.Web.Mail.MailMessage> objets peuvent inclure des caractères non-ASCII. Dans le .NET Framework 4, seuls les caractères ASCII sont pris en charge. <xref:System.Web.Mail.MailMessage> les objets qui contiennent des caractères non-ASCII et qui sont sérialisés sous le .NET Framework 4.5 ou version ultérieure ne peut pas être désérialisés sous le .NET Framework 4.|
|Suggestion|Assurez-vous que votre code fournit la gestion des exceptions lors de la désérialisation d’un <xref:System.Web.Mail.MailMessage> objet.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Web.Mail.MailMessage?displayProperty=nameWithType></li></ul>|

