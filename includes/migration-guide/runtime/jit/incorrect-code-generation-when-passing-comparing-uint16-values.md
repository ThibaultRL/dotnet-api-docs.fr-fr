### <a name="incorrect-code-generation-when-passing-and-comparing-uint16-values"></a>Génération de code incorrecte lors de la transmission et en comparant les valeurs de UInt16

|   |   |
|---|---|
|Détails|En raison de modifications introduites dans le 4.7 Framework .NET, dans certains cas le code généré par le compilateur JIT dans les applications qui s’exécutent sur le 4.7 Framework .NET incorrectement compare deux <code>T:System.UInt16</code> valeurs. Pour plus d’informations, consultez [problème #11508 : silencieux codegen incorrect lors de la transmission et comparaison ushort args](https://github.com/dotnet/coreclr/issues/11508) sur GitHub.com.|
|Suggestion|Si vous rencontrez des problèmes lors de la comparaison des valeurs non signées de 16 bits dans le 4.7 Framework .NET, mettez à niveau vers le Kit de développement .NET Framework 4.7.1.|
|Portée|Microsoft Edge|
|Version|4.7|
|Type|Runtime|

