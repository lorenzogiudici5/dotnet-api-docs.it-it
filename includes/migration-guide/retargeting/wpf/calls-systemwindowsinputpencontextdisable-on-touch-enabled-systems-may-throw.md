### <a name="calls-to-systemwindowsinputpencontextdisable-on-touch-enabled-systems-may-throw-an-argumentexception"></a>Chiamate a System.Windows.Input.PenContext.Disable nei sistemi abilitato per il tocco potrebbero generare un'eccezione ArgumentException

|   |   |
|---|---|
|Dettagli|In alcuni casi, le chiamate a interna <strong>System.Windows.Intput.PenContext.Disable</strong> metodo nei sistemi abilitato per il tocco potrebbe generare non gestito <code>T:System.ArgumentException</code> a causa della reentrancy.|
|Suggerimento|Questo problema è stato risolto in 4.7 il Framework .NET. Per evitare l'eccezione, eseguire l'aggiornamento a una versione di .NET Framework a partire dal 4.7 di .NET Framework.|
|Ambito|Microsoft Edge|
|Versione|4.6.1|
|Tipo|Ridestinazione|

