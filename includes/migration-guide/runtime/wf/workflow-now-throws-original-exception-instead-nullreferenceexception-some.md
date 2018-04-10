### <a name="workflow-now-throws-original-exception-instead-of-nullreferenceexception-in-some-cases"></a>Flux de travail présent lève une exception d’origine au lieu de l’exception NullReferenceException dans certains cas

|   |   |
|---|---|
|Détails|Dans le .NET Framework 4.6.2 et les versions antérieures, lorsque la méthode d’exécution d’une activité de workflow lève une exception avec un <code>null</code> la valeur pour le <xref:System.Exception.Message> propriété, le runtime de flux de travail System.Activities lève un <xref:System.NullReferenceException?displayProperty=name>, masquage le exception d’origine. Dans le 4.7 .NET Framework, l’exception précédemment masquée est levée.|
|Suggestion|Si votre code repose sur la gestion de la <xref:System.NullReferenceException?displayProperty=name>, modifiez-le afin d’intercepter les exceptions qui peuvent être levées à partir de vos activités personnalisées.|
|Portée|Mineur|
|Version|4.7|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Activities.CodeActivity.Execute(System.Activities.CodeActivityContext)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity%601.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.WorkflowInvoker.Invoke?displayProperty=nameWithType></li></ul>|

