### <a name="assemblies-compiled-with-regexcompiletoassembly-breaks-between-40-and-45"></a>Assemblys compilés avec sauts Regex.CompileToAssembly entre 4.0 et 4.5

|   |   |
|---|---|
|Détails|Si un assembly d’expressions régulières compilées est généré avec le .NET Framework 4.5, mais la cible le .NET Framework 4, essayez d’utiliser l’une des expressions régulières dans la mesure où l’assembly sur un système avec .NET Framework 4 est installé lève une exception.|
|Suggestion|Pour contourner ce problème, vous pouvez procéder de l'une des manières suivantes :<ul><li>Générez l’assembly qui contient les expressions régulières .NET Framework 4.</li><li>Utilisez une expression régulière interprétée.</li></ul>|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName)?displayProperty=nameWithType></li><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName,System.Reflection.Emit.CustomAttributeBuilder[])?displayProperty=nameWithType></li><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName,System.Reflection.Emit.CustomAttributeBuilder[],System.String)?displayProperty=nameWithType></li></ul>|

