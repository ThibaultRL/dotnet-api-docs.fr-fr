### <a name="workflowdesignerload-doesnt-remove-symbol-property"></a>WorkflowDesigner.Load ne supprime pas la propriété de symbole

|   |   |
|---|---|
|Détails|Lorsque vous ciblez le .NET Framework 4.5 dans le Concepteur de flux de travail et le chargement d’un flux de travail 3.5 hébergé à nouveau avec le <xref:System.Activities.Presentation.WorkflowDesigner.Load> (méthode), un <xref:System.Xaml.XamlDuplicateMemberException?displayProperty=name> est levée lors de l’enregistrement du flux de travail.|
|Suggestion|Ce bogue manifestes uniquement lorsque vous ciblez .NET Framework 4.5 dans le Concepteur de flux de travail, afin qu’il peut être contourné en définissant le <code>WorkflowDesigner.Context.Services.GetService&lt;DesignerConfigurationService&gt;().TargetFrameworkName</code> à le Framework.Alternatively .NET 4.0, le problème peut être évité grâce à la <xref:System.Activities.Presentation.WorkflowDesigner.Load(System.String)> méthode pour charger le flux de travail au lieu de <xref:System.Activities.Presentation.WorkflowDesigner.Load>.|
|Portée|Majeur|
|Version|4.5|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Activities.Presentation.WorkflowDesigner.Load?displayProperty=nameWithType></li></ul>|

