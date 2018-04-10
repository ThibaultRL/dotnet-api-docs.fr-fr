### <a name="itemsclear-does-not-remove-duplicates-from-selecteditems"></a>Items.Clear ne supprime pas les doublons de SelectedItems

|   |   |
|---|---|
|Détails|Supposons qu’un sélecteur (avec la sélection multiple est activée) a des doublons son <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> collection - le même élément apparaît plusieurs fois.  Suppression de ces éléments à partir de la source de données (par exemple, en appelant Items.Clear) ne parvient pas à les supprimer à partir de <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>; uniquement la première instance est supprimée. En outre, une utilisation ultérieure de <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> (par exemple, SelectedItems.Clear()) peuvent rencontrer des problèmes tels que <xref:System.ArgumentException?displayProperty=name>, car <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> contient des éléments qui ne sont plus dans la source de données.|
|Suggestion|Mise à niveau si possible vers .NET 4.6.2.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=nameWithType></li></ul>|

