### <a name="applicationfiltermessage-no-longer-throws-for-re-entrant-implementations-of-imessagefilterprefiltermessage"></a>Application.FilterMessage ne lève plus pour les implémentations réentrantes de IMessageFilter.PreFilterMessage

|   |   |
|---|---|
|Détails|Avant le .NET Framework 4.6.1, en appelant <xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)> avec un <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)> qui appelée <xref:System.Windows.Forms.Application.AddMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name> ou <xref:System.Windows.Forms.Application.RemoveMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name> (tout en appelant <xref:System.Windows.Forms.Application.DoEvents>) provoquerait une <xref:System.IndexOutOfRangeException?displayProperty=name>. À partir des applications qui ciblent le .NET Framework 4.6.1, cette exception ne soit plus levée et rentrant comme décrit ci-dessus peut utiliser des filtres.|
|Suggestion|N’oubliez pas que <xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)> n’est plus lève pour le réentrante <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)> comportement décrit ci-dessus. Cela affecte uniquement les applications qui ciblent le .NET Framework 4.6.1.Apps ciblant le .NET Framework 4.6.1 peut refuser cette modification (ou les applications ciblant des infrastructures plus anciens peuvent s’abonner) à l’aide de la [DontSupportReentrantFilterMessage](~/docs/framework/migration-guide/mitigation-custom-imessagefilter-prefiltermessage-implementations.md#mitigation) commutateur de compatibilité.|
|Portée|Microsoft Edge|
|Version|4.6.1|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)?displayProperty=nameWithType></li></ul>|

