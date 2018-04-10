### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>L’exception NullReferenceException dans le code à partir de ImageSourceConverter.ConvertFrom de gestion des exceptions

|   |   |
|---|---|
|Détails|Une erreur dans le code de gestion des exceptions <xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)> a provoqué un incorrect <xref:System.NullReferenceException?displayProperty=name> levée au lieu de l’exception prévue (par exemple, <xref:System.IO.DirectoryNotFoundException?displayProperty=name>, <xref:System.IO.FileNotFoundException?displayProperty=name>), cette modification résout cette erreur afin que la méthode lève maintenant la bonne exception. En valeur par défaut de toutes les applications qui ciblent .NET Framework 4.6.2 et ci-dessous continuera à lever <xref:System.NullReferenceException?displayProperty=name> pour assurer la compatibilité, les développeurs ciblant .NET Framework 4.7 et versions ultérieures doit voir le droit exceptions.// remplacer l’espace par un « x », le cas échéant|
|Suggestion|Les développeurs qui souhaitent revenir à la mise en route <xref:System.NullReferenceException?displayProperty=name> lorsque ciblant .NET Framework 4.7 permettre ajouter et de fusion suivantes au fichier App.config de l’application :<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.7|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|

