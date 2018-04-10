### <a name="systemthreadingtaskstask-no-longer-throw-objectdisposedexception-after-object-is-disposed"></a>System.Threading.Tasks.Task ne lèvent plus ObjectDisposedException après suppression de l’objet

|   |   |
|---|---|
|Détails|À l’exception de <xref:System.Threading.Tasks.Task.System%23IAsyncResult%23AsyncWaitHandle>, <xref:System.Threading.Tasks.Task?displayProperty=name> méthodes ne lèvent plus un <xref:System.ObjectDisposedException?displayProperty=name> exception une fois que l’objet est supprimé. Cette modification prend en charge l’utilisation des tâches de mise en cache. Par exemple, une méthode peut retourner une tâche mise en cache pour représenter une opération déjà terminée au lieu d'allouer une nouvelle tâche. Cette opération était impossible dans les versions précédentes du .NET Framework, car tout consommateur de la tâche pouvait la supprimer, ce qui la rendait inutilisable.|
|Suggestion|Sachez que les méthodes de la tâche peuvent lever n’est plus <xref:System.ObjectDisposedException?displayProperty=name> dans les cas où l’objet est supprimé. Si une application a été en fonction de savoir qu’une tâche a été supprimée de cette exception, il doit être mis à jour pour vérifier explicitement l’état de la tâche à l’aide de <xref:System.Threading.Tasks.Task.Status>.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|

