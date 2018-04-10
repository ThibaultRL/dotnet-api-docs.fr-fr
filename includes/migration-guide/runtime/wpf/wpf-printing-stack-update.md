### <a name="wpf-printing-stack-update"></a>Mise à jour de pile de l’impression WPF

|   |   |
|---|---|
|Détails|À l’aide des API de l’impression de WPF <xref:System.Printing.PrintQueue?displayProperty=name> maintenant appeler des API de Package de la fenêtre Imprimer Document en faveur de l’API d’impression XPS désormais déconseillé. La modification a été effectuée avec la facilité de maintenance à l’esprit ; ni les utilisateurs ni les développeurs doivent voir toutes les modifications de comportement ou l’utilisation de l’API. La nouvelle pile d’impression est activée par défaut lors de l’exécution de mise à jour des créateurs de Windows 10. La pile d’impression ancien toujours continue de fonctionner exactement comme précédemment dans les versions antérieures de Windows.|
|Suggestion|Pour utiliser la pile ancien dans la mise à jour de Windows 10 créateurs, définissez la <code>UseXpsOMPrinting</code> valeur REG_DWORD de le <code>HKEY_CURRENT_USER\Software\Microsoft\.NETFramework\Windows Presentation Foundation\Printing</code> clé de Registre <code>1</code>.|
|Portée|Microsoft Edge|
|Version|4.7|
|Type|Runtime|

