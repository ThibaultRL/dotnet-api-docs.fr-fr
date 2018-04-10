### <a name="wpf-textbox-defaults-to-undo-limit-of-100"></a>Valeurs par défaut de la zone de texte WPF pour annuler la limite de 100

|   |   |
|---|---|
|Détails|Dans le .NET 4.5, le nombre maximal d’annulations d’opérations pour une zone de texte WPF est de 100 par défaut (dans le .NET 4.0, ce nombre était illimité).|
|Suggestion|Si une limite de l’annulation de 100 est trop faible, la limite peut être définie explicitement avec <xref:System.Windows.Controls.Primitives.TextBoxBase.UndoLimit>|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|

