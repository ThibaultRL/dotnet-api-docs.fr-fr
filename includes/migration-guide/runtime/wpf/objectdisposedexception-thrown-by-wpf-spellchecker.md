### <a name="objectdisposedexception-thrown-by-wpf-spellchecker"></a>ObjectDisposedException levée par le vérificateur orthographique WPF

|   |   |
|---|---|
|Détails|Applications WPF arrêtera parfois pendant l’arrêt de l’application avec un <xref:System.ObjectDisposedException?displayProperty=name> levée par le vérificateur d’orthographe. Il est résolu dans .NET 4.7 WPF par la gestion de l’exception en douceur et donc vous assurer que les applications sont affectées ne sont plus négatif. Il convient de noter que les exceptions de première chance occasionnelles continue à observer dans les applications en cours d’exécution sous un débogueur.|
|Suggestion|Mise à niveau vers .NET 4.7|
|Portée|Microsoft Edge|
|Version|4.6.1|
|Type|Runtime|

