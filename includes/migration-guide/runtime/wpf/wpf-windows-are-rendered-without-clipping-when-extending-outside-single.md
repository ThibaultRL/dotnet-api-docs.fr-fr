### <a name="wpf-windows-are-rendered-without-clipping-when-extending-outside-a-single-monitor"></a>Les fenêtres WPF sont restitués sans découpage lors de l’extension en dehors d’un même écran

|   |   |
|---|---|
|Détails|Dans le .NET Framework 4.6 en cours d’exécution sur Windows 8 et versions ultérieures, la totalité de la fenêtre est restituée sans découpage lorsqu’elle s’étend en dehors d’un affichage unique dans un scénario à plusieurs écrans. Cela est différent des versions précédentes du .NET Framework qui serait clip fenêtres WPF qui étendu au-delà d’un affichage unique.|
|Suggestion|Ce comportement (que ce soit découper ou non) peut être défini explicitement à l’aide de la <code>&lt;EnableMultiMonitorDisplayClipping&gt;</code> élément <code>&lt;appSettings&gt;</code> dans le fichier de configuration d’une application, ou en définissant le <code>EnableMultiMonitorDisplayClipping</code> propriété au démarrage de l’application.|
|Portée|Mineur|
|Version|4.6|
|Type|Runtime|

