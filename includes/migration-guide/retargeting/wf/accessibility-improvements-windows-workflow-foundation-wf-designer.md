### <a name="accessibility-improvements-in-windows-workflow-foundation-wf-workflow-designer"></a>Miglioramenti all'accessibilità nella finestra di progettazione del flusso di lavoro Windows Workflow Foundation (WF)

|   |   |
|---|---|
|Dettagli|La finestra di progettazione del flusso di lavoro Windows Workflow Foundation (WF) miglioramenti sul suo funzionamento con le tecnologie di accesso facilitato. Questi miglioramenti includono le seguenti modifiche:<ul><li>L'ordine di tabulazione viene modificato da sinistra a destra e dall'alto verso il basso in alcuni controlli:</li><li>La finestra di correlazioni di inizializzazione per l'impostazione dati di correlazione per il <xref:System.ServiceModel.Activities.InitializeCorrelation> attività</li><li>La finestra di definizione del contenuto per il <xref:System.ServiceModel.Activities.Receive>, <xref:System.ServiceModel.Activities.Send>, <xref:System.ServiceModel.Activities.SendReply>, e <xref:System.ServiceModel.Activities.ReceiveReply> attività</li><li>Altre funzioni sono disponibili tramite la tastiera:</li><li>Quando si modificano le proprietà di un'attività, gruppi di proprietà possono essere compressi tramite tastiera la prima volta che sono con stato attivo.</li><li>Icone di avviso sono ora accessibile dalla tastiera.</li><li>Pulsante più proprietà nella finestra proprietà è accessibile dalla tastiera.</li><li>Gli utenti della tastiera possono ora accedere agli elementi intestazione nei riquadri di argomenti e variabili della finestra di progettazione del flusso di lavoro.</li><li>Una maggiore visibilità degli elementi con lo stato attivo, ad esempio quando:</li><li>Aggiunta di righe alle griglie di dati utilizzate dai progettisti Progettazione flussi di lavoro e attività.</li><li>Il tasto TAB attraverso i campi nel <xref:System.ServiceModel.Activities.ReceiveReply> e <xref:System.ServiceModel.Activities.SendReply> le attività.</li><li>Impostazione dei valori predefiniti per variabili o argomenti</li><li>Gli screen reader ora può riconoscere correttamente:</li><li>Punti di interruzione impostati nella finestra di progettazione del flusso di lavoro.</li><li>Il <xref:System.Activities.Statements.FlowSwitch%601>, <xref:System.Activities.Statements.FlowDecision>, e <xref:System.ServiceModel.Activities.CorrelationScope> le attività.</li><li>Il contenuto del <xref:System.ServiceModel.Activities.Receive> attività.</li><li>Il tipo di destinazione per il <xref:System.Activities.Statements.InvokeMethod> attività.</li><li>Combobox (eccezione) e la sezione infine il <xref:System.Activities.Statements.TryCatch> attività.</li><li>Casella combinata tipo di messaggio, la barra di divisione nella finestra Aggiungi inizializzatori di correlazione, la finestra di definizione del contenuto e la finestra di CorrelatesOn Defintion nelle attività di messaggistica (<xref:System.ServiceModel.Activities.Receive>, <xref:System.ServiceModel.Activities.Send>, <xref:System.ServiceModel.Activities.SendReply>, e <xref:System.ServiceModel.Activities.ReceiveReply>).</li><li>Macchina a stati esegue la transizione e le transizioni di destinazioni.</li><li>Le annotazioni e connettori nel <xref:System.Activities.Statements.FlowDecision> le attività.</li><li>Menu di scelta rapida (rapida) per le attività.</li><li>Editor dei valori di proprietà, il pulsante Cancella ricerca, per categoria e pulsanti di ordinamento alfabetico e la finestra di dialogo Editor espressioni nella griglia delle proprietà.</li><li>La percentuale di zoom nella finestra di progettazione del flusso di lavoro.</li><li>Il separatore <xref:System.Activities.Statements.Parallel> e <xref:System.Activities.Statements.Pick> le attività.</li><li>Il <xref:System.Activities.Statements.InvokeDelegate> attività.</li><li>La finestra Seleziona tipi per le attività di dizionario (<code>Microsoft.Activities.AddToDictionary&lt;TKey,TValue&gt;</code>, <code>Microsoft.Activities.RemoveFromDictionary&lt;TKey,TValue&gt;</code>, ecc.).</li><li>La finestra di esplorazione e Seleziona tipo di .NET.</li><li>Navigazione nella finestra di progettazione del flusso di lavoro.</li><li>Gli utenti che scelgono temi a contrasto elevato visualizzeranno numerosi miglioramenti introdotti nella visibilità della finestra di progettazione del flusso di lavoro e i relativi controlli come contrasto meglio rapporti tra gli elementi e le caselle di selezione più evidente usate per gli elementi lo stato attivo.</li></ul>|
|Suggerimento|Se si dispone di un'applicazione con una finestra di progettazione del flusso di lavoro ospitata nuovamente, l'applicazione può trarre vantaggio da queste modifiche eseguendo una di queste azioni:<ul><li>Ricompilare l'applicazione in .NET Framework 4.7.1 di destinazione. Queste modifiche di accessibilità sono abilitate per impostazione predefinita.</li><li>Se l'applicazione destinato a .NET Framework 4,7 o versioni precedenti, ma è in esecuzione in .NET Framework 4.7.1, è possibile rifiutare esplicitamente questi comportamenti accessibilità legacy aggiungendo quanto segue [AppContext commutatore](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) per il <code>&lt;runtime&gt;</code> sezione di App. config file e impostarlo su <code>false</code>, come illustrato nell'esempio seguente.</li></ul><pre><code>&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;&#13;&#10;&lt;configuration&gt;&#13;&#10;&lt;startup&gt;&#13;&#10;&lt;supportedRuntime version=&quot;v4.0&quot; sku=&quot;.NETFramework,Version=v4.7&quot;/&gt;&#13;&#10;&lt;/startup&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;!-- AppContextSwitchOverrides value attribute is in the form of &#39;key1=true/false;key2=true/false  --&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>Applicazioni destinate a .NET Framework 4.7.1 o versione successiva e si desidera mantenere legacy comportamento accessibilità può optare per l'utilizzo delle funzionalità di accessibilità legacy impostando in modo esplicito questa opzione AppContext su <code>true</code>.|
|Ambito|Secondario|
|Versione|4.7.1|
|Tipo|Ridestinazione|
