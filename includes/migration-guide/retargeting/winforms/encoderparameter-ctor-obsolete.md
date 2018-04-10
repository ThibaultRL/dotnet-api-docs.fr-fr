### <a name="encoderparameter-ctor-is-obsolete"></a>EncoderParameter ctor est obsolète

|   |   |
|---|---|
|Détails|Le constructeur <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)> est désormais obsolète et génère des avertissements quand il est utilisé.|
|Suggestion|Bien que le <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)>constructeur continueront de fonctionner, le constructeur suivant doit être utilisé à la place pour éviter l’avertissement de génération obsolète lors de la compilation de nouveau code à l’aide des outils de .NET 4.5 : <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Drawing.Imaging.EncoderParameterValueType,System.IntPtr)>.|
|Portée|Mineur|
|Version|4.5|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)?displayProperty=nameWithType></li></ul>|

