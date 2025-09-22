# Azure-Datawarehouse - Azure Blob(Raw File -object Storage)-> Azure DataFlow (Transformations)-> Azure Data Factory(Azure Data lake Gen2) ->Publish(Production)->Debug to check for any errors
Files related to sales and employees

Project Objective and Summary:

•  Developed a cloud-native data pipeline using Azure Data Factory (ADF) to automate the movement of raw CSV files from a Blob Storage landing zone to a curated zone in Azure Data Lake Gen2.
•  Configured Copy Data activities to ingest and route files, and implemented Mapping Data Flows to apply transformations including trimming and converting country names to lowercase using derived column expressions.
•  Validated and published pipeline components, ensuring robust connectivity between source and sink datasets with schema mapping and file format standardization.
•  Enabled event-based triggers to detect new file arrivals in Blob Storage and initiate automated processing, ensuring real-time data availability in the curated zone.
•  Ensured production readiness by verifying source/sink paths, testing pipeline logic via debug sessions, and monitoring execution through ADF’s built-in logging and alerting tools.
•  Delivered clean, structured data outputs optimized for analytics, reporting, and integration with downstream platforms such as Synapse, Power BI, or Databricks.

/pipelines/
  - transformEmpData.json
/datasets/
  - rawBlobDataset.json
  - curatedLakeDataset.json
/linkedServices/
  - blobStorageLS.json
  - dataLakeLS.json
/triggers/
  - fileArrivalTrigger.json
/armTemplates/
  - ARMTemplateForFactory.json
  - ARMTemplateParametersForFactory.json
