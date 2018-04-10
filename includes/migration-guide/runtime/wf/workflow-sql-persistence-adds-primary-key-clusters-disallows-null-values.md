### <a name="workflow-sql-persistence-adds-primary-key-clusters-and-disallows-null-values-in-some-columns"></a>Persistenza del flusso di lavoro aggiunge chiave primaria cluster e non consente valori null in alcune colonne

|   |   |
|---|---|
|Dettagli|A partire da 4.7 il Framework .NET, le tabelle create per l'archivio di istanza del flusso di lavoro (SWIS) SQL, tramite lo script Sqlworkflowinstancestoreschema utilizzano cluster le chiavi primarie. Per questo motivo, non supportano le identità <code>null</code> valori. L'operazione di SWIS non venga interessato da questa modifica. Gli aggiornamenti sono stati apportati per supportare la replica transazionale di SQL Server.|
|Suggerimento|Per poter esperienza questa modifica è necessario applicare il file SQL Sqlworkflowinstancestoreschemaupgrade alle installazioni esistenti. Le nuove installazioni di database avranno automaticamente la modifica.|
|Ambito|Microsoft Edge|
|Versione|4.7|
|Tipo|Runtime|

