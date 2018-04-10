### <a name="resizing-a-grid-can-hang"></a>Redimensionnement d’une grille peut se bloquer

|   |   |
|---|---|
|Détails|Une boucle infinie peut se produire lors de la disposition d’un <code>T:System.Windows.Controls.Grid</code> dans les circonstances suivantes :<ul><li>Définitions de ligne contiennent deux *-lignes, les deux déclarer un MinHeight et un MaxHeight.</li><li>Contenu de la *-lignes ne dépasse pas le MaxHeight correspondant</li><li>Hauteur disponible de la grille est dépassée par le premier MinHeight (plus n’importe quel autre fixe ou automatique les lignes)</li><li>L’application cible .net 4.7 ou a donné son consentement à l’algorithme de 4,7 allocation en définissant <code>Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=false</code></li></ul>La boucle est également se produire avec plus de deux lignes, ou dans le cas analogue pour les colonnes. Le problème est résolu dans .net 4.7.1.|
|Suggestion|Mise à niveau vers .net 4.7.1.  Vous pouvez également, si vous ne devez pas l’algorithme de 4.7 allocation, vous pouvez utiliser le paramètre de configuration suivant :<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.7|
|Type|Runtime|

