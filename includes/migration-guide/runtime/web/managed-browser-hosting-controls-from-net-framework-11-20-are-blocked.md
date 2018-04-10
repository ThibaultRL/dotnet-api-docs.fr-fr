### <a name="managed-browser-hosting-controls-from-the-net-framework-11-and-20-are-blocked"></a>Hébergement des contrôles managés de navigateur à partir de .NET Framework 1.1 et 2.0 sont bloqués.

|   |   |
|---|---|
|Détails|L'hébergement de ces contrôles est bloqué dans Internet Explorer.|
|Suggestion|Internet Explorer ne démarrera pas les applications qui utilisent des contrôles d'hébergement de navigateur géré. Le comportement précédent peut être restauré en définissant la valeur EnableIEHosting de la sous-clé de Registre <code>HKLM/SOFTWARE/MICROSOFT/.NETFramework</code> à <code>1</code> pour x86 systèmes et pour les processus 32 bits sur x64 systèmes et en définissant le <code>EnableIEHosting</code> valeur de la sous-clé de Registre <code>HKLM/SOFTWARE/Wow6432Node/Microsoft/.NETFramework</code>à <code>1</code> pour les processus 64 bits sur x64 systèmes.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|

