### <a name="wpf-textbox-selected-text-appears-a-different-color-when-the-text-box-is-inactive"></a>Texte de WPF de zone de texte sélectionnée apparaît dans une couleur différente de la zone de texte est inactive

|   |   |
|---|---|
|Détails|Dans le .NET 4.5, lorsqu’un contrôle de zone de texte WPF est inactif (c’est-à-dire qu’il n’a pas le focus), le texte sélectionné dans la zone s’affiche dans une couleur différente de celle utilisée lorsque le contrôle est actif.|
|Suggestion|Comportement (.NET 4.0) précédent peut être restauré en affectant la <xref:System.Windows.FrameworkCompatibilityPreferences.AreInactiveSelectionHighlightBrushKeysSupported> propriété <code>false</code>.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|

