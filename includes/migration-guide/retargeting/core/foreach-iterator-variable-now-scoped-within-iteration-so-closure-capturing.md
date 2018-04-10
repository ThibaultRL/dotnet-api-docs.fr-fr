### <a name="foreach-iterator-variable-is-now-scoped-within-the-iteration-so-closure-capturing-semantics-are-different-in-c5"></a>Variable d’itérateur foreach est désormais étendue au sein de l’itération, afin de la sémantique de capture de fermeture est différente (dans C# 5)

|   |   |
|---|---|
|Détails|À partir de c# 5 (Visual Studio 2012), <code>foreach</code> variables d’itération sont limités au sein de l’itération. Cela peut provoquer des sauts si le code a été précédemment selon les variables de ne pas être inclus dans le <code>foreach</code>de fermeture. Le problème de cette modification est qu’une variable d’itérateur passée à un délégué est traitée en tant que la valeur qu’au moment où le délégué est créée, au lieu de la valeur qu’au moment de que l’appel du délégué.|
|Suggestion|Dans l’idéal, le code doit être mis à jour pour prévoir ce nouveau comportement du compilateur. Si vous avez besoin de l’ancienne sémantique, la variable d’itérateur peut être remplacée par une autre variable placée explicitement en dehors de la portée de la boucle.|
|Portée|Majeur|
|Version|4.5|
|Type|Reciblage|

