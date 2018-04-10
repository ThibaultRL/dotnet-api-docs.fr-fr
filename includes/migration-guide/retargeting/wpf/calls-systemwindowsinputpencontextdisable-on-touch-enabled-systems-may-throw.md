### <a name="calls-to-systemwindowsinputpencontextdisable-on-touch-enabled-systems-may-throw-an-argumentexception"></a>Appels à System.Windows.Input.PenContext.Disable sur les systèmes de tactile peuvent lever une exception ArgumentException

|   |   |
|---|---|
|Détails|Dans certaines circonstances, les appels à interne <strong>System.Windows.Intput.PenContext.Disable</strong> méthode sur les systèmes de tactile peut lever une non gérée <code>T:System.ArgumentException</code> en raison de la réentrance.|
|Suggestion|Ce problème a été résolu dans le 4.7 Framework .NET. Pour empêcher cette exception, la mise à niveau vers une version du .NET Framework en commençant par le 4.7 Framework .NET.|
|Portée|Microsoft Edge|
|Version|4.6.1|
|Type|Reciblage|

