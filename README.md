# Azure Synapse Link for SQL Server 2022 Database Project

Example of a state-Based deployment for [Azure Synapse Link for SQL Server 2022](https://learn.microsoft.com/en-us/azure/synapse-analytics/synapse-link/sql-server-2022-synapse-link?WT.mc_id=DP-MVP-5004032).

It first stops the link running. It then deploys updates to a database running in SQL Server 2022 before starting the link again. Based on a blog post I wrote called '[A complete CI/CD experience for Azure Synapse Link for SQL Server 2022](https://www.kevinrchant.com/2022/10/20/a-complete-ci-cd-experience-for-azure-synapse-link-for-sql-server-2022/)'.

You can see this template in the [video for the March 2023 edition of the Azure Synapse Analytics and MVP series](https://www.youtube.com/watch?v=wakDmLYxSD0). Click on the link to view.

It contains an example YAML file that you can use as a YAML pipeline in Azure Pipelines. You can find it in the AzureDevOpsTemplates folder. In order to use it in Azure Pipelines you can either import or fork this repository into another GitHub repository, or into [Azure Repos](https://bit.ly/3s4uO77).

Afterwards, you can select the YAML file in Azure Pipelines and tailor the pipeline to suit your needs. You can find a guide on how to select the YAML file whilst setting up a YAML Pipeline this in a blog post I wrote called '[Connect a Database Project in Azure Repos to Azure Pipelines](https://bit.ly/3uF1Iv9)'.

You can find the recommended variables inside the YAML file. Avoid putting sensitive information directly into the YAML file (like your connection details). One thing I must stress here is that the password MUST be wrapped in single quotes in the secret for it to work.

You can use the logic in 'Classic Editor' instead by adding the tasks into the GUI and transferring the logic over. Alternatively, you can build an artifact for it using the 'Classic Editor' and use the 'Releases' feature for deployments. Personally, I prefer doing the deployment using a YAML pipeline.

This repository is provided "as is" based on the [MIT license](https://opensource.org/licenses/MIT). Basically, I am not responsible for your use of it.
