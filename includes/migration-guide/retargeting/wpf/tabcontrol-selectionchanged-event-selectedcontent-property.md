### <a name="tabcontrol-selectionchanged-event-and-selectedcontent-property"></a>Événement TabControl SelectionChanged et SelectedContent propriété

|   |   |
|---|---|
|Détails|En commençant par le .NET Framework 4.7.1, un <xref:System.Windows.Controls.TabControl> met à jour la valeur de sa <xref:System.Windows.Controls.TabControl.SelectedContent> propriété avant le déclenchement de le <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> événement, lors de sa sélection change. Dans le .NET Framework 4.7 et les versions antérieures, la mise à jour SelectedContent s’est produite après l’événement.|
|Suggestion|Les applications qui ciblent le .NET Framework 4.7.1 ou version ultérieure peuvent la refuser cette modification et utiliser le comportement hérité en ajoutant le code suivant à la <code>&lt;runtime&gt;</code> section du fichier de configuration d’application :<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Les applications qui ciblent le .NET Framework 4.7 ou antérieure mais sont en cours d’exécution sur le .NET Framework 4.7.1 ou version ultérieure peuvent activer le nouveau comportement en ajoutant la ligne suivante à la <code>&lt;runtime&gt;</code> section du fichier .configuration application :<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Portée|Mineur|
|Version|4.7.1|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Windows.Controls.TabControl.SelectedContent?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.Selector.SelectionChanged?displayProperty=nameWithType></li></ul>|

