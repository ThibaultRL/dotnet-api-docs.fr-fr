### <a name="profiling-aspnet-mvc4-apps-can-lead-to-fatal-execution-engine-error"></a>Les applications ASP.Net MVC 4 risque d’erreur irrécupérable du moteur d’exécution

|   |   |
|---|---|
|Détails|Les profileurs de l’utilisation d’assemblys avec NGEN /Profile peuvent se bloquer les applications ASP.NET MVC 4 profilées au démarrage avec un 'exécution du moteur une Exception irrécupérable'|
|Suggestion|Ce problème est résolu dans le .NET Framework 4.5.2. Vous pouvez également, le profileur peut éviter ce problème en spécifiant <code>COR_PRF_DISABLE_ALL_NGEN_IMAGES</code> dans son masque d’événement.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|

