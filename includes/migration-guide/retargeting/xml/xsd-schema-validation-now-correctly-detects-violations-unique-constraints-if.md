### <a name="xsd-schema-validation-now-correctly-detects-violations-of-unique-constraints-if-compound-keys-are-used-and-one-key-is-empty"></a>Validation de schéma XSD maintenant détecte correctement les violations de contraintes uniques si les clés composées sont utilisés et d’une clé est vide

|   |   |
|---|---|
|Détails|Les versions du .NET Framework antérieures à 4.6 contenaient un bogue qui empêchait la validation XSD de détecter les contraintes uniques des clés composées si l’une d’elles était vide. Dans le .NET Framework 4.6, ce problème est résolu. La validation est désormais plus précise. Toutefois, il se peut que du code XML ne soit plus validé, alors qu’il l’était dans les versions précédentes.|
|Suggestion|Si un contrôle de .NET Framework 4.0 est nécessaire, l’application de validation peut cibler la version 4.5 (ou antérieure) du .NET Framework. Toutefois, lorsque vous reciblez vers .NET 4.6, passez en revue le code pour vérifier que les clés composées en double (comme décrit plus haut) ne sont pas censées être validées.|
|Portée|Microsoft Edge|
|Version|4.6|
|Type|Reciblage|

