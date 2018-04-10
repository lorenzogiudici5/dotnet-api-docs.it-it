### <a name="null-coalescer-values-are-not-visible-in-debugger-until-one-step-later"></a>I valori di dispositivo null non sono visibili nel debugger fino a un unico passaggio in un secondo momento

|   |   |
|---|---|
|Dettagli|Un bug in .NET Framework 4.5 fa sì che i valori impostati tramite un'operazione coalescing null per non essere visibili nel debugger immediatamente dopo l'operazione di assegnazione viene eseguita quando in esecuzione la versione a 64 bit di Framework.|
|Suggerimento|L'esecuzione di istruzioni una volta aggiuntiva nel debugger causerà il locale/valore del campo da aggiornare in modo corretto. Inoltre, questo problema è stato risolto in .NET Framework 4.6; l'aggiornamento a tale versione di Framework dovrebbe risolvere il problema.|
|Ambito|Microsoft Edge|
|Versione|4.5|
|Tipo|Runtime|

