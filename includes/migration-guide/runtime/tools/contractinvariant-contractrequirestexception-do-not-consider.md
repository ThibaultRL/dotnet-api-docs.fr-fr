### <a name="contractinvariant-or-contractrequirestexception-do-not-consider-stringisnullorempty-to-be-pure"></a>Contract.Invariant ou Contract.Requires<TException> ne considérez pas String.IsNullOrEmpty comme pure

|   |   |
|---|---|
|Détails|Pour les applications qui ciblent le .NET Framework 4.6.1, si le nom invariant de contrat pour <xref:System.Diagnostics.Contracts.Contract.Invariant%2A?displayProperty=nameWithType> ou le contrat de condition préalable pour <xref:System.Diagnostics.Contracts.Contract.Requires%2A?displayProperty=nameWithType)> appelle la <xref:System.String.IsNullOrEmpty%2A?displayProperty=nameWithType> (méthode), le module de réécriture émet un avertissement CC1036 du compilateur : &quot;détecté d’appel de méthode ' System.String.IsNullOrWhteSpace(System.String)' sans [Pure] dans la méthode.&quot; Il s’agit d’un avertissement au lieu d’une erreur du compilateur du compilateur.|
|Suggestion|Ce comportement est abordé dans le [problème 339](https://github.com/Microsoft/CodeContracts/issues/339), sur le site GitHub. Pour éviter cet avertissement, vous pouvez télécharger et compilez une version mise à jour du code source pour l’outil de contrats de Code à partir de [GitHub](https://github.com/Microsoft/CodeContracts/blob/master/README.md). Des informations sur le téléchargement se trouvent au bas de la page.|
|Portée|Mineur|
|Version|4.6.1|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Diagnostics.Contracts.Contract.Invariant(System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Contracts.Contract.Requires(System.Boolean)?displayProperty=nameWithType></li></ul>|

