Utilizzando basati su caratteri l'indicizzazione con il <xref:System.Text.StringBuilder.Chars%2A> proprietà può essere molto lenta nelle condizioni seguenti:

- Il <xref:System.Text.StringBuilder> istanza è di grandi dimensioni (ad esempio, è costituito da diverse decine di migliaia di caratteri).
- Il <xref:System.Text.StringBuilder> è "voluminosi". Vale a dire, chiamate ripetute a metodi, ad esempio <xref:System.Text.StringBuilder.Append%2A?displayProperty=nameWithType> espansi automaticamente l'oggetto <xref:System.Text.StringBuilder.Capacity%2A?displayProperty=nameWithType> proprietà e allocati nuovi blocchi di memoria a esso.

Poiché l'accesso ogni carattere scorre l'intero elenco collegato di blocchi da memorizzare nel buffer corretti da indicizzare trovare gravemente sulle prestazioni.

> [!NOTE]
>  Anche per un grande "voluminose", <xref:System.Text.StringBuilder> dell'oggetto, utilizzando il <xref:System.Text.StringBuilder.Chars%2A> proprietà per l'accesso basato su indice a uno o un numero ridotto di caratteri ha un impatto trascurabile sulle prestazioni, ma in genere, è anche un **0(n)** operazione. L'impatto significativo sulle prestazioni si verifica quando si scorre i caratteri nel <xref:System.Text.StringBuilder> oggetto, ovvero un' **O(n^2)** operazione. 

Se si verificano problemi di prestazioni quando si utilizza basati su caratteri indicizzazione con <xref:System.Text.StringBuilder> oggetti, è possibile utilizzare una delle seguenti soluzioni alternative:

- Convertire il <xref:System.Text.StringBuilder> istanza a un <xref:System.String> chiamando il <xref:System.Text.StringBuilder.ToString%2A> (metodo), quindi accedere ai caratteri nella stringa.

- Copiare il contenuto dell'oggetto esistente <xref:System.Text.StringBuilder> ridimensionate preventivamente un nuovo oggetto <xref:System.Text.StringBuilder> oggetto. Migliora le prestazioni in quanto il nuovo <xref:System.Text.StringBuilder> oggetto non è "voluminoso". Ad esempio:

   ```csharp
   // sbOriginal is the existing StringBuilder object
   var sbNew = new StringBuilder(sbOriginal.ToString(), sbOriginal.Length);
   ```
   ```vb
   ' sbOriginal is the existing StringBuilder object
   Dim sbNew = New StringBuilder(sbOriginal.ToString(), sbOriginal.Length)
   ```
- Impostare la capacità iniziale del <xref:System.Text.StringBuilder> oggetto su un valore che corrisponde approssimativamente alle dimensioni massime previste chiamando il <xref:System.Text.StringBuilder.%23ctor(System.Int32)> costruttore. Si noti che questo viene allocato l'intero blocco anche se memoria il <xref:System.Text.StringBuilder> raramente raggiunge la capacità massima.
