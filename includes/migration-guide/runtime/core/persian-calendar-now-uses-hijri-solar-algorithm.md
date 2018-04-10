### <a name="persian-calendar-now-uses-the-hijri-solar-algorithm"></a>Calendario persiano ora utilizza l'algoritmo solare Hijri

|   |   |
|---|---|
|Dettagli|A partire da .NET Framework 4.6, il <xref:System.Globalization.PersianCalendar?displayProperty=name> classe Usa l'algoritmo solare Hijri. Conversione di date comprese tra il <xref:System.Globalization.PersianCalendar?displayProperty=name> altri calendari non possono restituire un risultato leggermente diverso partire da .NET Framework 4.6 per le date precedenti a 1800 o successive a 2023 (gregoriano). Inoltre, <xref:System.Globalization.PersianCalendar.MinSupportedDateTime> è ora <code>March 22, 0622 instead of March 21, 0622</code>.|
|Suggerimento|Tenere presente che alcune date precedenti o successive potrebbero essere leggermente diverse quando si usa PersianCalendar in .NET 4.6. Inoltre, quando si serializzano le date tra processi che possono essere eseguiti in versioni diverse di .NET Framework, evitare di archiviarle come stringhe di data PersianCalendar, perché tali valori potrebbero essere diversi.|
|Ambito|Secondario|
|Versione|4.6|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Globalization.PersianCalendar?displayProperty=nameWithType></li></ul>|

