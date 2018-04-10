### <a name="changing-the-isenabled-property-of-the-parent-of-a-textblock-control-affects-any-child-controls"></a>Modification de la propriété IsEnabled du parent d’un contrôle TextBlock affecte tous les contrôles enfants

|   |   |
|---|---|
|Détails|En commençant par le .NET Framework 4.6.2, la modification la <xref:System.Windows.UIElement.IsEnabled?displayProperty=name> propriété du parent d’un <xref:System.Windows.Controls.TextBlock?displayProperty=name> contrôle affecte tous les contrôles enfants (par exemple, les liens hypertexte et les boutons) de la <xref:System.Windows.Controls.TextBlock?displayProperty=name> contrôle. Dans .NET Framework 4.6.1 et versions antérieures, les contrôles à l’intérieur d’un <xref:System.Windows.Controls.TextBlock?displayProperty=name> ne pas toujours refléter l’état de la <xref:System.Windows.UIElement.IsEnabled?displayProperty=name> propriété de la <xref:System.Windows.Controls.TextBlock?displayProperty=name> parent.|
|Suggestion|Aucun. Cette modification est conforme au comportement attendu pour les contrôles à l’intérieur d’un contrôle <xref:System.Windows.Controls.TextBlock?displayProperty=name>.|
|Portée|Mineur|
|Version|4.6.2|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.UIElement.IsEnabled?displayProperty=nameWithType></li></ul>|

