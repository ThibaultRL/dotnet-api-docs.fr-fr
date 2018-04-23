### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>NullReferenceException dans le code de gestion des exceptions à partir de ImageSourceConverter.ConvertFrom

|   |   |
|---|---|
|Détails|Une erreur dans le code de gestion des exceptions pour <xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)> a provoqué la levée d’une exception <xref:System.NullReferenceException?displayProperty=name> incorrecte à la place de l’exception prévue (par exemple, <xref:System.IO.DirectoryNotFoundException?displayProperty=name>, <xref:System.IO.FileNotFoundException?displayProperty=name>). Ce changement résout cette erreur pour que la méthode lève la bonne exception. Par défaut, toutes les applications qui ciblent le .NET Framework 4.6.2 et antérieur continuent à lever l’exception <xref:System.NullReferenceException?displayProperty=name> à des fins de compatibilité. Les développeurs ciblant le .NET Framework 4.7 et ultérieur doivent voir les bonnes exceptions.// Remplacer l’espace par un « x » le cas échéant|
|Suggestion|Les développeurs qui ciblent le .NET Framework 4.7 et qui préfèrent obtenir l’exception <xref:System.NullReferenceException?displayProperty=name> peuvent ajouter/fusionner les éléments suivants dans le fichier App.config de leur application :<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.7|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|

