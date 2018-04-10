### <a name="building-an-entity-framework-edmx-with-visual-studio-2013-can-fail-with-error-msb4062-if-using-the-entitydeploysplit-or-entityclean-tasks"></a>Création d’un fichier edmx d’Entity Framework avec Visual Studio 2013 peut échouer avec l’erreur MSB4062 si vous utilisez les tâches EntityDeploySplit ou EntityClean

|   |   |
|---|---|
|Détails|Outils MSBuild 12.0 (inclus dans Visual Studio 2013) modifier les emplacements de fichier MSBuild, à l’origine des anciens fichiers de cibles d’Entity Framework n’est pas valide. Les tâches <code>EntityDeploySplit</code> et <code>EntityClean</code> échouent, car elles ne parviennent pas à trouver <code>Microsoft.Data.Entity.Build.Tasks.dll</code>. Notez que ce saut n’en raison d’une modification de l’ensemble d’outils (MSBuild/Visual Studio), en raison d’une modification de .NET Framework. Il est dû à la mise à niveau des outils de développement, et non à celle du .NET Framework.|
|Suggestion|Fichiers de cibles Entity Framework sont fixés pour travailler avec la nouvelle possibilité à compter de disposition MSBuild dans le .NET Framework 4.6. Vous pouvez résoudre ce problème en mettant à niveau votre .NET Framework vers la version 4.6. Vous pouvez également utiliser [cette solution de contournement](http://stackoverflow.com/a/24249247/131944) pour corriger directement les fichiers cibles.|
|Portée|Majeur|
|Version|4.5.1|
|Type|Reciblage|

