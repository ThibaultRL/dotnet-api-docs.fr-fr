### <a name="no-longer-able-to-set-enableviewstatemac-to-false"></a>N’est plus en mesure de définir EnableViewStateMac sur false

|   |   |
|---|---|
|Détails|ASP.NET ne permet plus aux développeurs de spécifier <code>&lt;pages enableViewStateMac=&quot;false&quot;/&gt;</code> ou <code>&lt;@Page EnableViewStateMac=&quot;false&quot; %&gt;</code>. Le code d'authentification de message (code MAC) de l'état d'affichage est à présent appliqué à toutes les demandes avec état d'affichage intégré. Seules les applications qui définira explicitement la propriété EnableViewStateMac à <code>false</code> sont affectées.|
|Suggestion|EnableViewStateMac doit être censé pour avoir la valeur true, et toutes les erreurs résultants de MAC doivent être résolus (comme expliqué dans [ce guide](https://support.microsoft.com/kb/2915218), qui contient plusieurs résolutions selon les spécificités de ce qui provoque des erreurs de MAC).|
|Portée|Majeur|
|Version|4.5.2|
|Type|Runtime|

