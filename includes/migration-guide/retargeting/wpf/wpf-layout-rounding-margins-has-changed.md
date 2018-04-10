### <a name="wpf-layout-rounding-of-margins-has-changed"></a>Arrondi de disposition WPF des marges a changé.

|   |   |
|---|---|
|Détails|La façon dont les marges sont arrondies, les bordures et l'arrière-plan ont changé. Résultat de cette modification :<ul><li>La largeur ou la hauteur d'éléments peut croître ou diminuer d'un pixel au plus.</li><li>La position d'un objet peut se déplacer d'un pixel au plus.</li><li>Les éléments centrés peuvent être décalés verticalement ou horizontalement d'un pixel au plus.</li></ul>Par défaut, cette nouvelle disposition est activée uniquement pour les applications qui ciblent le .NET. Framework 4.6.|
|Suggestion|Étant donné que cette modification tend à éliminer le découpage droit ou inférieur des contrôles WPF à dpi élevé, les applications qui ciblent des versions antérieures du .NET Framework mais sont exécutent sur le .NET Framework 4.6 peuvent adopter ce nouveau comportement en ajoutant la ligne suivante à la <code>&lt;runtime&gt;</code> section du fichier app.config : <code>&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.DoNotApplyLayoutRoundingToMarginsAndBorderThickness=false&quot; /&gt;</code>applications qui ciblent le .NET Framework 4.6, mais souhaitez que les contrôles WPF soient rendus à l’aide de l’algorithme de disposition précédent peuvent se faire en ajoutant la ligne suivante à la <code>&lt;runtime&gt;</code> section du fichier app.config : <code>&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.DoNotApplyLayoutRoundingToMarginsAndBorderThickness=true&quot; /&gt;</code>.|
|Portée|Mineur|
|Version|4.6|
|Type|Reciblage|

