
# Using Azure Synapse with Microsoft Power BI

This code will provive you a step-by-step guide to create a DataMart with transport information.

This DataMart is build using Azure Data Factory for ELT/ETL and Azure Synapse as database. The final stage of the entire solution is a Power BI report reading the information from DataMart.

Some really important aspects in the solution is how to take advantage of dynamic content in Azure Data Factoty, creating a clean solution from begining to end.

We will split the solution deployment in:

1. Create Azure Services.
2. Deploy database scripts.
3. Deploy Azure Data Factory ARM template.

Before start, we need to check all requirements:

## Requirements

- Access to Azure account with permission to create Azure services
- Permission to install PowerShell components in your local computer
- A Power BI Free or Pro license

# 1 - Create Azure Services

The Azure Services can be created in Azure Portal or executing PowerShell scripts:

[Scripts location](https://github.com/brunohca/Power-BI-ADF-Synapse/tree/patch-1/1%20-%20Setup%20-%20PowerShell%20scripts)

1.1 - Create resource group.ps1

2.2 - Create Storage Account.ps1

3.3 - Create Azure Synapse Workspace.ps1

4.4 - Create Azure SQL Pool.ps1

5.5 - Create Azure Data Factory.ps1

# 2 - Create Synapse objects

Once you create Azure services, is necessary to deploy Synapse objects. Please execute next steps:

[Scripts location](https://github.com/brunohca/Power-BI-ADF-Synapse/tree/patch-1/1%20-%20Setup%20database%20scripts)

1.1 - Create schemas.sql

2.2 - Create operational tables.sql

3.3 - Create data warehouse tables.sql

4.4 - Create stage tables.sql

5.5 - Create external tables.sql

6.6 - Insert dimensions data.sql

7.7 - Insert configuration table.sql

# 3 - Deploy ARM template

The Azure Services can be created in Azure Portal or executing PowerShell scripts:

# 4 - Others steps

Is necessary to upload a file into the storage account. Please fallow the instructions:

1.1 - Download file named "taxi_zone_lookup.csv": [Dowload CSV file](https://github.com/brunohca/Power-BI-ADF-Synapse/tree/patch-1/3)
2.2 - Upload file into this location in the storage account: "nyccabdata\ingestion\lookpup\taxi_zone_lookup.csv"
