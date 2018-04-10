### <a name="etw-event-names-cannot-differ-only-by-a-start-or-stop-suffix"></a>Les noms d’événements ETW ne peuvent pas différer uniquement par un suffixe « Start » ou « Arrêter »

|   |   |
|---|---|
|Détails|Dans le .NET Framework 4.6 et 4.6.1, le runtime lève une <xref:System.ArgumentException> lorsque les deux noms d’événements de suivi d’événements pour Windows (ETW) diffèrent uniquement par un &quot;Démarrer&quot; ou &quot;arrêter&quot; suffixe (comme quand un événement nommé <code>LogUser</code>et un autre est nommé <code>LogUserStart</code>). Dans ce cas, le runtime ne peut pas construire la source d’événements, qui ne peut pas émettre de journalisation.|
|Suggestion|Pour empêcher cette exception, vérifiez qu’aucun nom de deux événement ne diffère uniquement par un &quot;Démarrer&quot; ou &quot;arrêter&quot; suffixe. Cette exigence est supprimée, en commençant par le .NET Framework 4.6.2 ; le runtime peut lever l’ambiguïté des noms d’événements qui diffèrent uniquement par le &quot;Démarrer&quot; et &quot;arrêter&quot; suffixe.|
|Portée|Microsoft Edge|
|Version|4.6|
|Type|Reciblage|

