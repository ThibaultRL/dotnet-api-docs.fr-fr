### <a name="workflow-sql-persistence-adds-primary-key-clusters-and-disallows-null-values-in-some-columns"></a>Persistance de workflow SQL ajoute des clusters et n’autorise pas les valeurs null dans les colonnes de clé primaire

|   |   |
|---|---|
|Détails|À partir de la 4.7 Framework .NET, les tables créées pour la banque d’Instance du flux de travail SQL (SWIS) par le script SqlWorkflowInstanceStoreSchema.sql utilisent des clés primaires en cluster. Pour cette raison, les identités ne prennent pas en charge <code>null</code> valeurs. L’opération de SWIS n’est pas affectée par cette modification. Les mises à jour ont été apportées pour prendre en charge la réplication transactionnelle de SQL Server.|
|Suggestion|Le fichier SQL SqlWorkflowInstanceStoreSchemaUpgrade.sql doit être appliqué aux installations existantes afin de bénéficier de cette modification. Les nouvelles installations de base de données aura automatiquement la modification.|
|Portée|Microsoft Edge|
|Version|4.7|
|Type|Runtime|

