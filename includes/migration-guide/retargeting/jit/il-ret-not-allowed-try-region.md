### <a name="il-ret-not-allowed-in-a-try-region"></a>IL ret ne pas autorisée dans une région de try

|   |   |
|---|---|
|Détails|À la différence du compilateur juste-à-temps JIT64, RyuJIT (utilisé dans le .NET 4.6) n’autorise pas un IL ret instruction dans une région de try. Retour à partir d’une région de try n’est pas autorisée par la spécification ECMA-335 et aucun compilateur managé connu ne génère ce code IL. Toutefois, le compilateur JIT64 exécute ce code IL, s'il est généré à l'aide de l'émission de réflexion.|
|Suggestion|Si une application génère en langage intermédiaire qui inclut un opcode ret dans une région de try, l’application peut cibler .NET 4.5 pour utiliser l’ancien JIT et pour éviter ce saut de ligne. Ou bien, l’IL généré peut être mis à jour pour retourner après la région de try.|
|Portée|Microsoft Edge|
|Version|4.6|
|Type|Reciblage|

