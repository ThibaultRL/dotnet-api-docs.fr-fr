### <a name="marshalsizeof-and-marshalptrtostructure-overloads-break-dynamic-code"></a>Marshal.SizeOf et Marshal.PtrToStructure surcharges endommager le code dynamique

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.5.1, liaison dynamique aux méthodes <xref:System.Runtime.InteropServices.Marshal.SizeOf%60%601>, <xref:System.Runtime.InteropServices.Marshal.SizeOf%60%601(%60%600)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure(System.IntPtr,System.Object)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure(System.IntPtr,System.Type)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure%60%601(System.IntPtr)>, ou <xref:System.Runtime.InteropServices.Marshal.PtrToStructure%60%601(System.IntPtr,%60%600)>, (via Windows PowerShell, IronPython ou le langage c# mot clé dynamique, par exemple) vous risquez <code>MethodInvocationExceptions</code> nouvelles surcharges de ces méthodes ont été ajoutés, qui peuvent être ambiguës pour les moteurs de script.|
|Suggestion|Les scripts de mise à jour pour indiquer clairement la surcharge doivent être utilisées. Pour cela, castez explicitement les paramètres de type de la méthode en tant que <xref:System.Type>. Cliquez sur [ce lien](https://support.microsoft.com/kb/2909958/) pour plus de détails et d’exemples sur la manière de contourner ce problème.|
|Portée|Mineur|
|Version|4.5.1|
|Type|Runtime|

