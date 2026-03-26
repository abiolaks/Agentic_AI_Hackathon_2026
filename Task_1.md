
Lab Validation
More 

Challenge 01: Create the Microsoft Foundry AI Environment
Introduction
Before building intelligent AI agents, Contoso Wellness must first establish a reliable AI development environment. This environment will host the AI models, vector search service, and project workspace required to build and run the Health & Fitness Assistant.

Microsoft Foundry provides a centralized platform for deploying models, managing connections, and building AI-powered applications. In this challenge, you will create the core infrastructure required for the lab, including an Azure AI Search service, a Foundry hub and project, and several AI models that will power the assistant’s reasoning and retrieval capabilities.

Once these resources are deployed, the environment will be ready for developing AI workflows and agent-based applications.

Challenge Objectives
Create an Azure AI Search service for vector-based retrieval
Create a Microsoft Foundry hub and project
Deploy the required AI models for the workshop
Configure resource connections within the project
Steps to Complete
Create Azure AI Search
In the Azure Portal.

In the search bar, type AI Search, then select AI Search from the results.

Click + Create.

Configure the search service using the following values:

Subscription: Select the default Subscription.

Resource Group: Select challenge-rg-2151676

Service Name: aisearch-2151676

Location: swedencentralswedencentral

Pricing Tier: Basic

Note: If the swedencentralswedencentral region does not have quota available, choose from any of the available region.

Click Review + Create, then click Create.

Wait for the deployment to complete.

Note: Azure AI Search deployment may take 10–15 minutes depending on the region.

Once deployment finishes, open the AI Search resource and verify that the service is active.

Create Bing Resources
In the Azure Portal.

In the search bar, type Bing Resources, then select Bing Resources from the results.

Click + Add.

Select Grounding with Bing Search.

Provide the following details:

Resource Group: Select challenge-rg-2151676
Name: bing-search-2151676
Pricing tier: Grounding with Bing Search ($14 per 1K transactions)
Terms: Select the checkbox to accept the terms.
Click Review + Create, then click Create.

Create the Microsoft Foundry Hub
In the Azure Portal, search for Microsoft Foundry and select it.

In the Use with Foundry tab, click on AI Hubs.

Click on + Create and select Hub.

Configure the Azure AI Hub:

Subscription: Select the default Subscription.
Resource Group: challenge-rg-2151676
Region: swedencentralswedencentral
Name: Ai-Hub-2151676
Leave the remaining to default values.
Click Review + Create, then click Create.

Wait for the deployment to complete.

Once the deployment is ready, click on Go to resource.

Create the Foundry Project
Now, on the Azure AI hub page that appears, click on + Create project.

Provide the following value:

Subscription: Select the default Subscription.
Resource Group: challenge-rg-2151676
Name: AI-Project-2151676
Leave the remaining to default values.
Click Review + Create, then click Create.

Wait for the deployment to complete.

Once the deployment is ready, click on Go to resource.

Now click Launch studio from the Overview section.

In the project overview page, copy the Project connection string and store it in a notepad file. This will be required in later challenges.

Deploy the GPT Model
In Microsoft Foundry portal.

Click on Models + Endpoints from the left navigation menu.

Click on + Deploy model and select Deploy base model.

Search for and select gpt-4.1 from the model catalog and click on Confirm button.

Configure the deployment:

Deployment name: keep the default name.

Deployment type: Global Standard

Click Customize.

Tokens per Minute Rate Limit: 50K

Important: Do not increase the TPM limit beyond 50K to avoid exceeding quota limits and additional costs.

Select Connect and deploy.

Deploy the Embedding Model
Click again on Models + Endpoints from the left navigation menu.

Click on + Deploy model and select Deploy base model.

Search for and select text-embedding-3-large from the model catalog and click on Confirm button.

Configure the deployment:

Deployment name: keep the default name.

Deployment type: Global Standard

Click Customize.

Tokens per Minute Rate Limit: 50K

Important: Do not increase the TPM limit beyond 50K to avoid exceeding quota limits and additional costs.

Select Connect and deploy.

Deploy the DeepSeek-R1 Model
Click again on Models + Endpoints from the left navigation menu.

Click on + Deploy model and select Deploy base model.

Search for and select DeepSeek-R1 from the model catalog and click on Confirm button.

If a pop-up appears, click on Agree and Proceed.

Configure the deployment:

Deployment name: DeepSeek-R1

Deployment type: Global Standard

Click Customize.

Tokens per Minute Rate Limit: 50K

Important: Do not increase the TPM limit beyond 50K to avoid exceeding quota limits and additional costs.

Click on Deploy.

Deploy the Phi-4 Model
Click again on Models + Endpoints from the left navigation menu.

Click on + Deploy model and select Deploy base model.

Search for and select Phi-4 from the model catalog and click on Confirm button.

Select Azure AI Foundry models for the purchase options.

Click on Agree and Proceed.

Configure the deployment:

Deployment name: Phi-4
Deployment type: Global Standard
Click on Deploy.

Configure Project Connections
From the left navigation menu, select Management center.

Under Connected resources section select + New connection.

Search for Azure AI Search, then select Azure AI Search.

Search for the Azure AI Search service you created, aisearch-2151676. Choose API key as authentication and then select Add connection.

Make sure that AI Search shows Connected status.

Click Close once the connection is created.

Add Bing Grounding Connection
Click on + New connection again.

Search for Azure Grounding with Bing Search, then select it.

Search for the Bing Resource you created, bing-search-2151676. Choose API key as authentication and then select Add connection.

Make sure that AI Search shows Connected status.

Click Close once the connection is created.

Copy the OpenAI Service Connection Name
Navigate to the Manage connected resources in this hub page within the Connected resources under the Hub section from the left navigation menu.

Click on the Azure OpenAI connection name to open its details.

On the Connection Details page, copy the full connection name displayed at the top and store it in a notepad file. This will be required in later challenges.

Note: The connection name usually ends with _aoai (for example, aihub21xxxxxx119_aoai).

Add User Permission
From the left navigation menu under Hub, select Users.

Click + New user.

Enter the following username:

odl_user_2151676@cloudlabssandbox.onmicrosoft.comodl_user_2151676@cloudlabssandbox.onmicrosoft.com

Set the Role to Owner.

Click Add.

VALIDATION CHECK
Challenge 01: Create the Microsoft Foundry AI Environment
Status: Success
Congratulations on completing the Challenge! Now, it's time to validate it. Here are the steps:

Hit the Validate button for the corresponding Challenge. If you receive a success message, you can proceed to the next Challenge.
If not, carefully read the error message and retry the step, following the instructions in the lab guide.
If you need any assistance, please contact us at cloudlabs-support@spektrasystems.com. We are available 24/7 to help.
Success Criteria
Azure AI Search service deployed successfully
Microsoft Foundry hub and project created
gpt-model, text embedding, DeepSeek-R1, and Phi-4 models deployed
Azure AI Search and Bing grounding connections configured
Additional Resources
https://learn.microsoft.com/azure/ai-studio
https://learn.microsoft.com/azure/ai-services/openai
