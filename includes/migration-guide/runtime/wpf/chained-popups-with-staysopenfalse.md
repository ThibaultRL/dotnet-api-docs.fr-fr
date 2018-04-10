### <a name="chained-popups-with-staysopenfalse"></a>Chaînées les fenêtres contextuelles avec StaysOpen = False

|   |   |
|---|---|
|Détails|Une fenêtre contextuelle avec StaysOpen = False est supposée se ferme lorsque vous cliquez en dehors de la fenêtre contextuelle. Lorsque deux ou plusieurs de ces messages sont chaînées (autrement dit, un contient un autre), a de nombreux problèmes, notamment :<ul><li>Ouvrez les deux niveaux, cliquez en dehors de P2, mais à l’intérieur de P1.  Rien ne se produit.</li><li>Ouvrez les deux niveaux, cliquez sur extérieur P1.  Les deux fenêtres contextuelles fermer.</li><li>Ouvrir et fermer les deux niveaux.  Réessayez d’ouvrir P2 à nouveau.  Rien ne se produit.</li><li>Essayez d’ouvrir des trois niveaux.  Tu peux pas.  (Rien ne se passe ou les deux premiers niveaux fermer, selon l’endroit où vous cliquez.) Ces cas (et autres variantes) désormais fonctionner comme prévu.</li></ul>|
|Portée|Microsoft Edge|
|Version|4.7.1|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Controls.Primitives.Popup.StaysOpen?displayProperty=nameWithType></li></ul>|

