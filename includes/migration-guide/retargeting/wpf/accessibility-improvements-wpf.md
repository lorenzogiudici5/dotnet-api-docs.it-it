### <a name="accessibility-improvements-in-wpf"></a>Miglioramenti all'accessibilità in WPF

|   |   |
|---|---|
|Dettagli|<strong>Miglioramenti a contrasto elevati</strong><ul><li>Lo stato attivo per il <xref:System.Windows.Controls.Expander> controllo è ora visibile. Nelle versioni precedenti di .NET Framework, non era.</li><li>Il testo nella <xref:System.Windows.Controls.CheckBox> e <xref:System.Windows.Controls.RadioButton> controlli quando vengono selezionati è ora più semplice visualizzare più nelle versioni precedenti di .NET Framework.</li><li>Il bordo di disattivato <xref:System.Windows.Controls.ComboBox> è lo stesso colore del testo disabilitato. Nelle versioni precedenti di .NET Framework, non era.</li><li>Pulsanti disabilitati e con lo stato attivo, ora, usare il colore del tema corretto. Nelle versioni precedenti di .NET Framework, non le supportavano.</li><li>Pulsante a discesa è ora visibile quando un <xref:System.Windows.Controls.ComboBox> stile del controllo è impostato su <xref:System.Windows.Controls.ToolBar.ComboBoxStyleKey?displayProperty=nameWithType>, nelle versioni precedenti di .NET Framework, non è stato.</li><li>La freccia di indicatore di ordinamento in un <xref:System.Windows.Controls.DataGrid> controllo Usa ora i colori del tema. Nelle versioni precedenti di .NET Framework non è stato eseguito.</li><li>Lo stile di un collegamento ipertestuale predefinito diventa ora il colore del tema corretto al passaggio del mouse. Nelle versioni precedenti di .NET Framework non è stato eseguito.</li><li>Lo stato attivo su pulsanti di opzione è ora visibile. Nelle versioni precedenti di .NET Framework, non era.</li><li>Il <xref:System.Windows.Controls.DataGrid> colonna del controllo casella di controllo Usa ora i colori previsto per il feedback lo stato attivo della tastiera. Nelle versioni precedenti di .NET Framework non è stato eseguito.</li><li>gli oggetti visivi dello stato attivo della tastiera sono ora visibili sul <xref:System.Windows.Controls.ComboBox> e <xref:System.Windows.Controls.ListBox>. Nelle versioni precedenti di .NET Framework, non era.</li></ul><strong>Miglioramenti di interazione lettura dello schermo</strong><ul><li><xref:System.Windows.Controls.Expander> i controlli sono ora correttamente ha annunciati come gruppi (Espandi/Comprimi) lettura dello schermo.</li><li><xref:System.Windows.Controls.DataGridCell> i controlli vengono ora correttamente annunciati come cella della griglia di dati (localizzato) lettura dello schermo.</li><li>Gli screen reader annuncerà ora il nome di un modificabile <xref:System.Windows.Controls.ComboBox>.</li><li><xref:System.Windows.Controls.PasswordBox> i controlli non siano annunciati come &quot;alcun elemento nella visualizzazione&quot; lettura dello schermo.</li></ul><strong>Supporto LiveRegion</strong>Screen Reader, ad esempio Assistente vocale consentono agli utenti di conoscere il contenuto dell'interfaccia utente di un'applicazione, in genere descrivendo un elemento sull'interfaccia utente che è attualmente attivo, perché è probabile che l'elemento di maggior interesse all'utente. Tuttavia, se un elemento dell'interfaccia utente viene modificato in qualche punto nella schermata e non è lo stato attivo, l'utente potrebbe non essere informati e perdere le informazioni importanti. LiveRegions servono solo per risolvere il problema. Uno sviluppatore può utilizzare per informare la lettura dello schermo o qualsiasi altro [automazione][Panoramica di automazione dell'interfaccia utente](~/docs/framework/ui-automation/ui-automation-overview.md) client che è stata apportata una modifica importante per un elemento dell'interfaccia utente. L'utilità per la lettura dello schermo può quindi decidere come e quando informare l'utente di questa modifica. La proprietà LiveSetting consente inoltre la lettura dello schermo di conoscere il livello di importanza per informare l'utente della modifica apportata all'interfaccia utente.|
|Suggerimento|<strong>Come partecipare o meno queste modifiche</strong>affinché l'applicazione per trarre vantaggio da queste modifiche, è necessario eseguita su .NET Framework 4.7.1 o versione successiva. L'applicazione può trarre vantaggio da queste modifiche in uno dei modi seguenti:<ul><li>Viene ricompilato destinato a .NET Framework 4.7.1. Queste modifiche di accessibilità sono abilitate per impostazione predefinita nelle applicazioni WPF destinati a .NET Framework 4.7.1 o versione successiva.</li><li>Rifiuta esplicitamente i comportamenti di accessibilità legacy aggiungendo quanto segue [AppContext commutatore](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) nel <code>&lt;runtime&gt;</code> sezione del file di configurazione dell'app e impostarlo su false, come illustrato nell'esempio seguente.</li></ul><pre><code>&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;&#13;&#10;&lt;configuration&gt;&#13;&#10;&lt;startup&gt;&#13;&#10;&lt;supportedRuntime version=&quot;v4.0&quot; sku=&quot;.NETFramework,Version=v4.7&quot;/&gt;&#13;&#10;&lt;/startup&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;!-- AppContextSwitchOverrides value attribute is in the form of &#39;key1=true/false;key2=true/false  --&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>Applicazioni destinate a .NET Framework 4.7.1 o versione successiva e si desidera mantenere legacy comportamento accessibilità può optare per l'utilizzo delle funzionalità di accessibilità legacy impostando in modo esplicito questa opzione AppContext su <code>true</code>. Per una panoramica di automazione interfaccia utente, vedere la [Panoramica di automazione dell'interfaccia utente](~/docs/framework/ui-automation/ui-automation-overview.md).|
|Ambito|Principale|
|Versione|4.7.1|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.Windows.Automation.AutomationElementIdentifiers.LiveSettingProperty?displayProperty=nameWithType></li><li><xref:System.Windows.Automation.AutomationElementIdentifiers.LiveRegionChangedEvent?displayProperty=nameWithType></li><li><xref:System.Windows.Automation.AutomationLiveSetting?displayProperty=nameWithType></li><li><xref:System.Windows.Automation.AutomationProperties.LiveSettingProperty?displayProperty=nameWithType></li><li><xref:System.Windows.Automation.AutomationProperties.SetLiveSetting(System.Windows.DependencyObject,System.Windows.Automation.AutomationLiveSetting)?displayProperty=nameWithType></li><li><xref:System.Windows.Automation.AutomationProperties.GetLiveSetting(System.Windows.DependencyObject)?displayProperty=nameWithType></li><li><xref:System.Windows.Automation.Peers.AutomationPeer.GetLiveSettingCore?displayProperty=nameWithType></li></ul>|
