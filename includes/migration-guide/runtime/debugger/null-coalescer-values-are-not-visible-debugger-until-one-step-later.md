### <a name="null-coalescer-values-are-not-visible-in-debugger-until-one-step-later"></a>Les valeurs NULL antémémoire ne sont pas visibles dans le débogueur jusqu'à une étape ultérieure

|   |   |
|---|---|
|Détails|Un bogue dans le .NET Framework 4.5 entraîne des valeurs définies via une opération de fusion null ne soit ne pas visible dans le débogueur immédiatement après l’exécution de l’opération d’assignation lors de l’exécution de la version 64 bits de l’infrastructure.|
|Suggestion|Pas à pas détaillé d’une seule fois supplémentaire dans le débogueur entraînera la local/valeur du champ à mettre à jour correctement. En outre, ce problème a été résolu dans le .NET Framework 4.6 ; la mise à niveau vers cette version du Framework devrait résoudre le problème.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|

