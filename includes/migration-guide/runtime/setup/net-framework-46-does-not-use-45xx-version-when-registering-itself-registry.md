### <a name="the-net-framework-46-does-not-use-a-45xx-version-when-registering-itself-in-the-registry"></a>Le .NET Framework 4.6 n’utilise pas une version 4.5.x.x lors de son enregistrement dans le Registre

|   |   |
|---|---|
|Détails|Comme l’indique, la clé de version définie dans le Registre (à <code>HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\NET Framework Setup\NDP\v4\Full</code>) pour le .NET Framework 4.6 commence par « 4.6', pas 4.5. Les applications qui dépendent de ces clés de Registre pour savoir quelles versions de .NET Framework sont installées sur un ordinateur doivent être mis à jour afin de comprendre que 4.6 est une nouvelle version possible, et qui est compatible avec la précédente 4.5.x libère.|
|Suggestion|Les applications de mise à jour recherchant un .NET Framework 4.5 installent en recherchant des clés de Registre 4.5 également accepter 4.6.|
|Portée|Microsoft Edge|
|Version|4.6|
|Type|Runtime|

