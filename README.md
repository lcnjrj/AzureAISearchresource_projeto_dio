# AzureAISearchresource_projeto_dio
Readme.md descrevendo o passo a passo para se configurar uma pesquisa


Create an Azure AI Search resource
Sign into the Azure portal.

Click the + Create a resource button, search for Azure AI Search, and create a Azure AI Search resource with the following settings:

Subscription: Your Azure subscription.
Resource group: Select or create a resource group with a unique name.
Service name: A unique name.
Location: Choose any available region.
Pricing tier: Basic
Select Review + create, and after you see the response Validation Success, select Create.

After deployment completes, select Go to resource. On the Azure AI Search overview page, you can add indexes, import data, and search created indexes.

Create an Azure AI services resource
You’ll need to provision an Azure AI services resource that’s in the same location as your Azure AI Search resource. Your search solution will use this resource to enrich the data in the datastore with AI-generated insights.

Return to the home page of the Azure portal. Click the ＋Create a resource button and search for Azure AI services. Select create an Azure AI services plan. You will be taken to a page to create an Azure AI services resource. Configure it with the following settings:
Subscription: Your Azure subscription.
Resource group: The same resource group as your Azure AI Search resource.
Region: The same location as your Azure AI Search resource.
Name: A unique name.
Pricing tier: Standard S0
By checking this box I acknowledge that I have read and understood all the terms below: Selected
Select Review + create. After you see the response Validation Passed, select Create.

Wait for deployment to complete, then view the deployment details.

Create a storage account
Return to the home page of the Azure portal, and then select the + Create a resource button.

Search for storage account, and create a Storage account resource with the following settings:
Subscription: Your Azure subscription.
Resource group: The same resource group as your Azure AI Search and Azure AI services resources.
Storage account name: A unique name.
Location: Choose any available location.
Performance: Standard
Redundancy: Locally redundant storage (LRS)
Click Review and then click Create. Wait for deployment to complete, and then go to the deployed resource.

In the Azure Storage account you created, in the left-hand menu pane, select Configuration (under Settings).
Change the setting for Allow Blob anonymous access to Enabled and then select Save.











Search explorer json
