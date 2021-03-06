## Deploy from Azure


You will need to create a service principal in order to use the 'Deploy from Azure' buttons.


For detailed instructions on deploying from Azure, including how to setup the service principal, see [Consuming: Deploy from Azure](../../consuming.md#deploy-from-azure)

### Simple deployment


<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fendjin%2FCNAB.Quickstarts%2Fmaster%2Fporter%2Fsql-server-always-on%2Fazuredeploy-simple.json" target="_blank"><img src="https://raw.githubusercontent.com/endjin/CNAB.Quickstarts/master/images/Deploy-from-Azure.png"/></a>

### Advanced deployment


<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fendjin%2FCNAB.Quickstarts%2Fmaster%2Fporter%2Fsql-server-always-on%2Fazuredeploy-advanced.json" target="_blank"><img src="https://raw.githubusercontent.com/endjin/CNAB.Quickstarts/master/images/Deploy-from-Azure.png"/></a>


## Deploy from Cloud Shell


For detailed instructions on deploying from Cloud Shell, including how to setup the Cloud Shell environment, see [Consuming: Deploy from Cloud Shell](../../consuming.md#deploy-from-cloud-shell)


```porter install --tag cnabquickstarts.azurecr.io/porter/sql-server-always-on:0.1.2 -d azure```


## Parameters and Credentials

 | Name | Description | Default | Required | 
 | --- | --- | --- | --- | 
 | aks_cluster_name | The name to use for the AKS Cluster |  | No
aks_resource_group | The name of the resource group to create the AKS Cluster in |  | No
azure_client_id | AAD Client ID for Azure account authentication - used for AKS Cluster SPN details and for authentication to azure to get KubeConfig - also if using ACI Driver  its used to authenticate to Azure for ACI creation to run bundle |  | Yes
azure_client_secret | AAD Client Secret for Azure account authentication - used for AKS Cluster SPN details and for authentication to azure to get KubeConfig - also if using ACI Driver  its used to authenticate to Azure for ACI creation to run bundle |  | Yes
azure_subscription_id | Azure Subscription Id used to set the subscription where the account has access to multiple subscriptions |  | Yes
azure_tenant_id | Azure AAD Tenant Id for Azure account authentication - used to authenticate to Azure to get KubeConfig |  | Yes
location | The Location to create the resources in |  | Yes
porter-debug | Print debug information from Porter when executing the bundle |  | No
sql_masterkeypassword | The Password for the SQL Server Master Key |  | Yes
sql_sapassword | The Password for the sa user in SQL Server |  | Yes | 
