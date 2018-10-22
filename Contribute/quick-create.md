---
title: 'Quickstart: Set and retrieve a secret from Azure Key Vault | Microsoft Docs'
description: 'Quickstart: Set and retrieve a secret from Azure Key Vault'
services: key-vault
author: syntaxc4
manager: erifkin
ms.date: 07/24/2018
ms.author: cfowler
zone_pivot_groups: keyvault-languages
ROBOTS: NOINDEX, NOFOLLOW
---

# Quickstart: Set and retrieve a secret from Azure Key Vault

This quickstart shows you how to store a secret in Key Vault and how to retrieve it using a Web app. To see the secret value you would have to run this on Azure. The quickstart uses Node.js and Managed service identities (MSIs).

> [!div class="checklist"]
> * Create a Key Vault.
> * Store a secret in the Key Vault.
> * Retrieve a secret from Key Vault.
> * Create an Azure Web Application.
> * [Enable managed service identities](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).
> * Grant the required permissions for the web application to read data from Key vault.

Before you proceed make sure that you are familiar with the [basic concepts](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).

> [!NOTE]
> To understand why the below tutorial is the best practice we need to understand a few concepts. Key Vault is a central repository to store secrets programmatically. But to do so applications / users need to first authenticate to Key Vault i.e. present a secret. To follow security best practices this first secret needs to be rotated periodically as well. But with [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview), applications that run in Azure are given an identity which is automatically managed by Azure. This helps solve the **Secret Introduction Problem** where users / applications can follow best practices and not have to worry about rotating the first secret

## Prerequisites

::: zone pivot="nodejs"
* [Node JS](https://nodejs.org/en/)
::: zone-end
::: zone pivot="dotnet"
* [Visual Studio 2017 version 15.7.3 or later](https://www.microsoft.com/net/download/windows) with the following workloads:
  * ASP.NET and web development
  * .NET Core cross-platform development
* [.NET Core 2.1 SDK or later](https://www.microsoft.com/net/download/windows)
::: zone-end
* Git ([download](https://git-scm.com/downloads)).
* An Azure subscription. If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.
* [Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) version 2.0.4 or later. This is available for Windows, Mac, and Linux.

## Login to Azure

To log in to Azure using the CLI, you can type:

```azurecli
az login
```

## Create resource group

Create a resource group with the [az group create](/cli/azure/group#az-group-create) command. An Azure resource group is a logical container into which Azure resources are deployed and managed.

Please select a Resource Group name and fill in the placeholder.
The following example creates a resource group named *<YourResourceGroupName>* in the *eastus* location.

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

The resource group you just created is used throughout this tutorial.

## Create an Azure Key Vault

Next you create a Key Vault using the resource group created in the previous step. Although “ContosoKeyVault” is used as the name for the Key Vault throughout this article, you have to use a unique name. Provide the following information:

* Vault name - **Select a Key Vault Name here**.
* Resource group name - **Select a Resource Group Name here**.
* The location - **East US**.

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

At this point, your Azure account is the only one authorized to perform any operations on this new vault.

## Add a secret to key vault

We're adding a secret to help illustrate how this works. You could be storing a SQL connection string or any other information that you need to keep securely but make available to your application. In this tutorial, the password will be called **AppSecret** and will store the value of **MySecret** in it.

Type the commands below to create a secret in Key Vault called **AppSecret** that will store the value **MySecret**:

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

To view the value contained in the secret as plain text:

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

This command shows the secret information including the URI. After completing these steps, you should have a URI to a secret in an Azure Key Vault. Write this information down. You need it in a later step.

## Clone the Repo

Clone the repo in order to make a local copy for you to edit the source by running the following command:

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

::: zone pivot="nodejs"

## Install dependencies

Here we install the dependencies. Run the following commands:

    cd key-vault-node-quickstart
    npm install

This project used 2 node modules:

* [ms-rest-azure](https://www.npmjs.com/package/ms-rest-azure) 
* [azure-keyvault](https://www.npmjs.com/package/azure-keyvault)

## Publish the web application to Azure

Below are the few steps we need to do to publish the application to Azure.

* The 1st step is to create a [Azure App Service](https://azure.microsoft.com/services/app-service/) Plan. You can store multiple web apps in this plan.

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* Next we create a web app. In the following example, replace <app_name> with a globally unique app name (valid characters are a-z, 0-9, and -). The runtime is set to NODE|6.9. To see all supported runtimes, run `az webapp list-runtimes`

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    When the web app has been created, the Azure CLI shows output similar to the following example:

    ```json
    {
      "availabilityState": "Normal",
      "clientAffinityEnabled": true,
      "clientCertEnabled": false,
      "cloningInfo": null,
      "containerSize": 0,
      "dailyMemoryTimeQuota": 0,
      "defaultHostName": "<app_name>.azurewebsites.net",
      "enabled": true,
      "deploymentLocalGitUrl": "https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git"
      < JSON data removed for brevity. >
    }
    ```
    Browse to your newly created web app and you should see a functioning web app. Replace <app_name> with a unique app name.

    ```text
    http://<app name>.azurewebsites.net
    ```
    The above command also creates a Git-enabled app which allows you to deploy to azure from your local git. 
    Local git is configured with url of 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git'

* Create a deployment user
    After the previous command is completed you can add add an Azure remote to your local Git repository. Replace <url> with the URL of the Git remote that you got from Enable Git for your app.

    ```bash
    git remote add azure <url>
    ```
    
::: zone-end

::: zone pivot="dotnet"
## Open and edit the solution

Edit the program.cs file to run the sample with your specific key vault name:

1. Browse to the folder key-vault-dotnet-core-quickstart.
2. Open the key-vault-dotnet-core-quickstart.sln file in Visual Studio 2017.
3. Open the Program.cs file and update the placeholder *YourKeyVaultName* with the name of your key vault that you created earlier.

This solution uses [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) and [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet libraries.

## Run the app

From the main menu of Visual Studio 2017, select **Debug** > **Start** without debugging. When the browser appears, go to the **About** page. The value for **AppSecret** is displayed.

## Publish the web application to Azure

Publish this app to Azure to see it live as a web app, and to see that you can fetch the secret value:

1. In Visual Studio, select the **key-vault-dotnet-core-quickstart** project.
2. Select **Publish** > **Start**.
3. Create a new **App Service**, and then select **Publish**.
4. Change the app name to **keyvaultdotnetcorequickstart**.
5. Select **Create**.

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]
::: zone-end

## Enable managed service identities

Azure Key Vault provides a way to securely store credentials and other keys and secrets, but your code needs to authenticate to Azure Key Vault to retrieve them. Managed Service Identity makes this easier by giving Azure services an automatically managed identity in Azure Active Directory (Azure AD). You can use this identity to authenticate to any service that supports Azure AD authentication, including Key Vault, without having any credentials in your code.

1. Return to the Azure CLI.
2. Run the assign-identity command to create the identity for this application:

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
>The command in this procedure is the equivalent of going to the portal and switching **Managed service identity** to **On** in the web application properties.

## Assign permissions to your application to read secrets from Key Vault

Make a note of the output when you publish the application to Azure. It should be of the format:

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

Then, run this command by using the name of your key vault and the value of **PrincipalId**:

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

::: zone pivot="nodejs"
## Deploy the Node App to Azure and retrieve the secret value

Now that everything is set. Run the following command to deploy the app to Azure

```bash
git push azure master
```

After this when you browse https://<app_name>.azurewebsites.net you can see the secret value.
Make sure that you replaced the name <YourKeyVaultName> with your vault name

::: zone-end

::: zone pivot="dotnet"
Now when you run the application, you should see your secret value retrieved.
::: zone-end

## Next steps

::: zone pivot="nodejs"
* [Azure Key Vault Home Page](https://azure.microsoft.com/services/key-vault/)
* [Azure Key Vault Documentation](https://docs.microsoft.com/azure/key-vault/)
* [Azure SDK For Node](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* [Azure REST API Reference](https://docs.microsoft.com/rest/api/keyvault/)
::: zone-end

::: zone pivot="dotnet"
* [Azure Key Vault home page](https://azure.microsoft.com/services/key-vault/)
* [Azure Key Vault documentation](https://docs.microsoft.com/azure/key-vault/)
* [Azure SDK For .NET](https://github.com/Azure/azure-sdk-for-net)
* [Azure REST API reference](https://docs.microsoft.com/rest/api/keyvault/)
::: zone-end
