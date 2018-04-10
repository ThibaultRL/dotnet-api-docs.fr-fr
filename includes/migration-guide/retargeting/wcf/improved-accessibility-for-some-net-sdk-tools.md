### <a name="improved-accessibility-for-some-net-sdk-tools"></a>Une meilleure accessibilité pour certains outils de développement .NET SDK

|   |   |
|---|---|
|Détails|Dans le .NET Framework SDK 4.7.1, les outils svcconfigedit.exe et svctraceviewer.exe ont été améliorés en corrigeant les divers niveaux d’accessibilité. La plupart d'entre elles étaient petits problèmes comme un nom non défini ou certains modèles UI automation ne pas implémentés correctement. Alors que de nombreux utilisateurs ne pourraient être prenant en charge de ces valeurs incorrectes, les clients qui utilisent les technologies d’assistance comme les lecteurs d’écran Rechercher ces outils du Kit de développement logiciel plus accessible. Certes, ces correctifs modifier certains comportements précédentes, comme l’ordre de focus clavier. Pour obtenir tous les correctifs de l’accessibilité dans ces outils, vous pouvez les éléments suivants à votre fichier app.config :<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.7.1|
|Type|Reciblage|

