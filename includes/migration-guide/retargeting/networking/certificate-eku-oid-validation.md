### <a name="certificate-eku-oid-validation"></a>Validation OID EKU du certificat

|   |   |
|---|---|
|Détails|Depuis .NET Framework 4.6, la <xref:System.Net.Security.SslStream> ou <xref:System.Net.ServicePointManager> classes valident une utilisation améliorée de la clé (EKU) objet (OID) d’identificateur. Une extension de l’utilisation de clé améliorée (EKU) est une collection d’identificateurs d’objet (OID) qui indiquent les applications qui utilisent la clé. Validation de l’OID EKU utilise des rappels de certificat à distance pour vous assurer que le certificat distant a les OID corrects pour l’utilisation prévue.|
|Suggestion|Si cette modification n’est pas souhaitable, vous pouvez désactiver la validation de l’OID EKU du certificat en ajoutant ce qui suit basculer vers le [ \<AppContextSwitchOverrides >](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) dans les [ ` ](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) de votre fichier de configuration d’application :<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Net.DontCheckCertificateEKUs=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre> <blockquote> [!IMPORTANT] Ce paramètre est fourni pour la compatibilité descendante uniquement. Son utilisation est déconseillée dans le cas contraire.</blockquote> |
|Portée|Mineur|
|Version|4.6|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Net.Security.SslStream?displayProperty=nameWithType></li><li><xref:System.Net.ServicePointManager?displayProperty=nameWithType></li><li><xref:System.Net.Http.HttpClient?displayProperty=nameWithType></li><li><xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType></li><li><xref:System.Net.HttpWebRequest?displayProperty=nameWithType></li><li><xref:System.Net.FtpWebRequest?displayProperty=nameWithType></li></ul>|

