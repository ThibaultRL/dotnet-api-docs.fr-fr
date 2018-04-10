### <a name="wpf-spell-checking-in-text-enabled-controls-will-not-work-in-windows-10-for-languages-not-in-the-oss-input-language-list"></a>Correction orthographique WPF dans les contrôles de texte activé ne fonctionne pas dans Windows 10 pour les langues pas dans la liste de langue d’entrée du système d’exploitation

|   |   |
|---|---|
|Détails|Lors de l’exécution sur Windows 10, le vérificateur d’orthographe peuvent ne pas fonctionne pour les contrôles WPF avec texte activé, car les fonctionnalités de vérification orthographique de plateforme sont disponibles uniquement pour les langues présentes dans la liste des langues d’entrée. Dans Windows 10, lorsqu’une langue est ajoutée à la liste des claviers disponibles, Windows télécharge et installe automatiquement correspondant de fonctionnalités sur le package à la demande (DOM) qui fournit des fonctionnalités de vérification orthographique. En ajoutant la langue à la liste des langues d'entrée, le vérificateur d'orthographe est pris en charge.|
|Suggestion|N’oubliez pas que la langue ou le texte à effectuer une vérification orthographique doit être ajouté comme langue d’entrée pour la vérification orthographique de travail dans Windows 10.|
|Portée|Microsoft Edge|
|Version|4.6|
|Type|Runtime|

