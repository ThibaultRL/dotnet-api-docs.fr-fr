### <a name="corprfgcroothandles-are-not-being-enumerated-by-profilers"></a>COR_PRF_GC_ROOT_HANDLEs ne sont pas énumérées par les profileurs

|   |   |
|---|---|
|Détails|Dans le .NET Framework v4.5.1, l’API de profilage <code>RootReferences2()</code> incorrectement jamais retourne <code>COR_PRF_GC_ROOT_HANDLE</code> (ils sont retournés en tant que <code>COR_PRF_GC_ROOT_OTHER</code> à la place). Ce problème est résolu à compter de .NET Framework 4.6.|
|Suggestion|Ce problème a été résolu dans le .NET Framework 4.6 et peut être adressé par la mise à niveau vers cette version du .NET Framework.|
|Portée|Mineur|
|Version|4.5.1|
|Type|Runtime|

