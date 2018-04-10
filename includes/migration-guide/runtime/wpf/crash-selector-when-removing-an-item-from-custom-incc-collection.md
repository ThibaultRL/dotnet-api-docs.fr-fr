### <a name="crash-in-selector-when-removing-an-item-from-a-custom-incc-collection"></a>Blocage dans le sélecteur lors de la suppression d’un élément à partir d’une collection INCC personnalisée

|   |   |
|---|---|
|Détails|Un <code>T:System.InvalidOperationException</code> peut se produire dans le scénario suivant :<ul><li>ItemsSource pour un <code>T:System.Windows.Controls.Primitives.Selector</code> est une collection avec une implémentation personnalisée de <code>T:System.Collections.Specialized.INotifyCollectionChanged</code>.</li><li>L’élément sélectionné est supprimé de la collection.</li><li>Le <code>T:System.Collections.Specialized.NotifyCollectionChangedEventArgs</code> a <code>P:System.Collections.Specialized.NotifyCollectionChangedEventArgs.OldStartingIndex</code> = -1 (indiquant une position inconnue).</li></ul>Pile des appels de l’exception commence à System.Windows.Threading.Dispatcher.VerifyAccess() à System.Windows.DependencyObject.GetValue (DependencyProperty dp) à System.Windows.Controls.Primitives.Selector.GetIsSelected (DependencyObject élément) cette exception peut se produire si l’application a plusieurs threads de répartiteur dans .net 4.5. L’exception peut également se produire dans les applications avec un seul thread de répartiteur dans .net 4.7. Le problème est résolu dans .net 4.7.1.|
|Suggestion|Mise à niveau vers .net 4.7.1.|
|Portée|Mineur|
|Version|4.7|
|Type|Runtime|

