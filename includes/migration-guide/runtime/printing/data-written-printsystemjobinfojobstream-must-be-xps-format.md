### <a name="data-written-to-printsystemjobinfojobstream-must-be-in-xps-format"></a>Les données écrites sur PrintSystemJobInfo.JobStream doivent être au format XPS

|   |   |
|---|---|
|Détails|Le <xref:System.Printing.PrintSystemJobInfo.JobStream> propriété expose le flux d’un travail d’impression. L’utilisateur peut envoyer des données brutes aux composants de l’impression de système d’exploitation sous-jacent en écrivant dans ce flux. À compter de .NET Framework 4.5 sur Windows 8 et versions ultérieures du système d’exploitation Windows, les données écrites dans ce flux doivent être au format XPS en tant que flux de package.|
|Suggestion|Pour sortir le contenu d’impression, vous pouvez procéder de l’une des manières suivantes :<ul><li>Utilisez la classe <xref:System.Windows.Xps.XpsDocumentWriter> pour sortir le contenu d’impression. Il s’agit de l’alternative recommandée.</li><li>Vérifiez que les données envoyées au flux retourné par la <xref:System.Printing.PrintSystemJobInfo.JobStream> propriété est au format XPS en tant que flux de package.</li></ul>|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Printing.PrintSystemJobInfo.JobStream?displayProperty=nameWithType></li></ul>|

