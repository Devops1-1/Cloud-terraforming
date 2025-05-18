Set Azure Creds
| Secret Name             | Purpose                            |
| ----------------------- | ---------------------------------- |
| `AZURE_CLIENT_ID`       | From `az ad sp` output             |
| `AZURE_CLIENT_SECRET`   | From `az ad sp` output             |
| `AZURE_TENANT_ID`       | From `az account show`             |
| `AZURE_SUBSCRIPTION_ID` | From `az account show`             |
| `ACR_NAME`              | Your Azure Container Registry name |
| `AKS_RESOURCE_GROUP`    | Resource group with your AKS       |
| `AKS_CLUSTER_NAME`      | Your AKS cluster name              |

Get Details of client and tenetid
az ad sp create-for-rbac --name "client-az" --role Contributor \
  --scopes /subscriptions/794523e6-3b17-47af-8859-54e18288c718 --sdk-auth