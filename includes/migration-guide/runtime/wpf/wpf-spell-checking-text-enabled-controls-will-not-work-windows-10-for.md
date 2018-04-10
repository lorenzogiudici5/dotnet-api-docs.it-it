### <a name="wpf-spell-checking-in-text-enabled-controls-will-not-work-in-windows-10-for-languages-not-in-the-oss-input-language-list"></a>Controllo ortografico nei controlli text abilitata WPF non funzionano in Windows 10 per le lingue non nell'elenco di lingua di input del sistema operativo

|   |   |
|---|---|
|Dettagli|Durante l'esecuzione in Windows 10, il controllo ortografico potrebbe non funzionare per i controlli WPF basate su testo perché le funzionalità di controllo ortografico della piattaforma sono disponibili solo per le lingue presenti nell'elenco delle lingue di input. In Windows 10, quando una lingua viene aggiunta all'elenco di tastiere disponibili, Windows automaticamente Scarica e installa una funzione corrispondente nel pacchetto di richiesta (DOM) che fornisce funzionalità di controllo ortografico. Aggiungendo la lingua all'elenco di lingue di input, il controllo ortografico sarà supportato.|
|Suggerimento|Tenere presente che è necessario aggiungere la lingua o il testo ortografico come lingua di input per il controllo ortografico per lavorare in Windows 10.|
|Ambito|Microsoft Edge|
|Versione|4.6|
|Tipo|Runtime|

