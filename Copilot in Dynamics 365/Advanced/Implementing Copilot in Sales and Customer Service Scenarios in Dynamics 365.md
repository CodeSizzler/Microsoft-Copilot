# Implementing Copilot in Sales and Customer Service Scenarios in Dynamics 365
## Overview
In this lab, you will learn how to use Copilot, a conversational AI assistant that helps sales and customer service agents to perform tasks and access information in Dynamics 365. Copilot is powered by Microsoft Bot Framework and Azure Cognitive Services, and can be integrated with various channels such as Teams, Outlook, or web chat. You will learn how to configure Copilot, train it with natural language understanding, and customize it with your own intents and dialogs.
## Prerequisites
To complete this lab, you will need the following:
- A Dynamics 365 trial environment with Sales and Customer Service apps installed. You can sign up for a free trial.
- An Azure subscription with sufficient credits to create a Bot Service and a Cognitive Services resource. You can sign up for a free trial.
- A Microsoft Teams account to test Copilot in Teams. You can sign up for a free account.
- A Power Platform account to access Power Apps and Power Automate. You can sign up for a free account.
- A GitHub account to clone the Copilot GitHub repository. You can sign up for a free account.
## Lab Steps
### Step 1: Clone the Copilot GitHub repository
The Copilot GitHub repository contains the source code, configuration files, and documentation for Copilot. You will need to clone the repository to your local machine to deploy and customize Copilot.
1. Open a web browser and navigate to URL.
2. Click on the **Code** button and select **Download ZIP**.
3. Save the ZIP file to your local machine and extract its contents to a folder of your choice.
4. Open the folder and explore the files and folders. You will see the following structure:
- **bot**: This folder contains the Bot Framework code for Copilot, written in C#.
- **cognitiveModels**: This folder contains the JSON files for the natural language understanding models for Copilot, powered by LUIS (Language Understanding Intelligent Service).
- **deploymentScripts**: This folder contains the PowerShell scripts for deploying Copilot to Azure.
- **dialogs**: This folder contains the JSON files for the dialogs for Copilot, powered by Adaptive Dialogs.
- **languageGeneration**: This folder contains the LG (Language Generation) files for the responses and prompts for Copilot.
- **[URL]**: This file contains the documentation for Copilot, including the prerequisites, deployment steps, and customization options.
### Step 2: Deploy Copilot to Azure
To deploy Copilot to Azure, you will need to run the PowerShell scripts in the deploymentScripts folder. These scripts will create and configure the Azure resources for Copilot, such as the Bot Service, the Cognitive Services, and the App Service.
1. Open a PowerShell window and navigate to the deploymentScripts folder.
2. Run the following command to install the Azure CLI, if you don't have it already:
```
Install-Module -Name Az -Scope CurrentUser -Repository PSGallery -Force
```
3. Run the following command to log in to your Azure account:
```
az login
```
4. Run the following command to create a resource group for Copilot in your Azure subscription. Replace {resourceGroupName} with a name of your choice, and {location} with a region of your choice, such as eastus or westeurope.
```
az group create --name {resourceGroupName} --location {location}
```
5. Run the following command to deploy Copilot to the resource group. Replace {resourceGroupName} with the name you used in the previous step, and {botName} with a name of your choice for the bot. This name must be unique across Azure, and can only contain alphanumeric characters and hyphens. The deployment may take several minutes to complete.
```
.\[URL] -resourceGroupName {resourceGroupName} -botName {botName}
```
6. After the deployment is completed, you will see a message with the following information:
- **Bot Service name**: The name of the Bot Service resource in Azure.
- **Bot Service endpoint**: The endpoint URL for the bot.
- **LUIS authoring key**: The key for the LUIS authoring resource in Azure.
- **LUIS endpoint key**: The key for the LUIS prediction resource in Azure.
- **LUIS app ID**: The ID of the LUIS app for Copilot.
- **QnA Maker subscription key**: The key for the QnA Maker resource in Azure.
- **QnA Maker endpoint**: The endpoint URL for the QnA Maker service.
- **QnA Maker KB ID**: The ID of the QnA Maker knowledge base for Copilot.
Copy and save this information, as you will need it later.
### Step 3: Train and publish the LUIS model for Copilot
To train and publish the LUIS model for Copilot, you will need to use the LUIS portal and the LUIS authoring key from the previous step. The LUIS model defines the intents and entities that Copilot can recognize from the user's input, such as createContact, updateOpportunity, or showDashboard.
1. Open a web browser and navigate to [URL].
2. Sign in with your Azure account and select the directory and subscription that contain the LUIS authoring resource for Copilot.
3. Click on the **My apps** tab and select the app named **Copilot-{botName}**, where {botName} is the name you used for the bot in the previous step.
4. You will see the LUIS app dashboard, where you can view and edit the intents, entities, and utterances for Copilot. You can also test the model by typing a query in the **Test your app** box on the right.
5. To train the model, click on the **Train** button on the top right. This will train the model with the existing data and generate a score for each intent and entity.
6. To publish the model, click on the **Publish** button on the top right. This will publish the model to the LUIS prediction resource in Azure, and generate an endpoint URL for the model.
7. Copy and save the endpoint URL, as you will need it later.
### Step 4: Test Copilot in the Azure portal
To test Copilot in the Azure portal, you will need to use the Bot Service resource and the Bot Service endpoint from the previous step. You can use the Test in Web Chat feature to interact with Copilot and see how it responds to your queries and commands.
1. Open a web browser and navigate to [URL].
2. Sign in with your Azure account and select the directory and subscription that contain the Bot Service resource for Copilot.
3. In the search box, type **Bot Services** and select the service from the results.
4. In the Bot Services page, select the bot named **{botName}**, where {botName} is the name you used for the bot in the previous step.
5. In the bot overview page, click on the **Test in Web Chat** option on the left menu.
6. You will see a web chat window, where you can type a message to Copilot and see its response. You can also see the JSON data for the message exchange in the **INSPECT** tab on the right.
7. Try typing some queries and commands to Copilot, such as:
- **Hi**: Copilot will greet you and ask for your name.
- **My name is {name}**: Copilot will remember your name and ask for your role.
- **I am a sales manager**: Copilot will acknowledge your role and show you some options to perform tasks or access information in Dynamics 365.
- **Show me the sales dashboard**: Copilot will open the sales dashboard in Dynamics 365 and show you some key metrics and charts.
- **Create a new contact**: Copilot will ask you for the details of the new contact, such as first name, last name, email, and phone number, and create the contact in Dynamics 365.
- **Update an opportunity**: Copilot will ask you for the name of the opportunity and the field you want to update, such as status, estimated revenue, or close date, and update the opportunity in Dynamics 365.
- **Help**: Copilot will show you a list of commands and topics it can handle, such as sales, customer service, or QnA.
### Step 5: Test Copilot in Teams
To test Copilot in Teams, you will need to use the Microsoft Teams app and the Bot Service name from the previous step. You can use the App Studio feature to create a custom app for Copilot and install it in Teams.
1. Open the Microsoft Teams app and sign in with your Teams account.
2. In the left menu, click on the **Apps** icon and search for **App Studio**.
3. Select the App Studio app and click on the **Open** button.
4. In the App Studio app, click on the **Manifest editor** tab and select **Create a new app**.
5. In the App details page, fill in the following information for Copilot:
- **App ID**: Generate a new app ID by clicking on the **Generate** button.
- **Name**: Enter a name for Copilot, such as **Copilot for Dynamics 365**.
- **Description**: Enter a short description for Copilot, such as **A conversational AI assistant for sales and customer service agents**.
- **Version**: Enter a version number for Copilot.
- **Short name**: Enter a short name for Copilot, such as **Copilot**.
- **App logo**: Upload an image file for Copilot, such as the Copilot logo from the GitHub repository.
6. In the left menu, click on the **Bots** option and select **Set up**.
7. In the Bot page, select **Existing bot** and enter the Bot Service name for Copilot, which is the same as the bot name you used in the previous steps.
8. Select **Personal** and **Team** as the scopes for Copilot, and click on the **Save** button.
9. In the left menu, click on the **Test and distribute** option and select **Install**.
10. In the Add app to team page, select **Add for you** and click on the **Add** button.
11. You will see a message that Copilot has been added to your personal apps in Teams.
12. In the left menu, click on the **Apps** icon and select **Copilot for Dynamics 365**.
13. You will see a chat window, where you can interact with Copilot in the same way as in the web chat.
14. You can also add Copilot to a team by selecting **Add to a team** in the Add app to team page, and choosing a team from the list. You can then mention Copilot in a team conversation by typing **@Copilot** and a query or command.
### Step 6: Customize Copilot with your own intents and dialogs
To customize Copilot with your own intents and dialogs, you will need to use the LUIS portal, the Bot Framework Composer, and the Copilot GitHub repository. You can add new intents and entities to the LUIS model, and create new dialogs and responses for Copilot using the Adaptive Dialogs and Language Generation features of the Bot Framework.
1. To add a new intent to the LUIS model, open the LUIS portal and select the Copilot app.
2. In the left menu, click on the **Intents** option and select **Create new intent**.
3. Enter a name for the new intent, such as **showCalendar**.
4. In the utterances box, enter some example sentences that express the new intent, such as:
- Show me my calendar
- What are my appointments for today?
- Open my schedule
5. Click on the **Train** and **Publish** buttons to update the LUIS model with the new intent.
6. To create a new dialog for the new intent, open the Bot Framework Composer and create a new bot project.
7. In the bot project, click on the **+** button and select **Add a new dialog**.
8. Enter a name for the new dialog, such as **ShowCalendarDialog**.
9. In the dialog design page, drag and drop a **Send a response** action from the left menu to the canvas.
10. In the **Language Generation** box, enter a response for the new dialog, such as:
- Sure, let me show you your calendar for today.
11. Drag and drop an **Open a URL** action from the left menu to the canvas, below the **Send a response** action.
12. In the **URL** box, enter the URL for opening the calendar in Dynamics 365, such as:
13. Save the dialog and test it in the emulator.
14. To integrate the new dialog with Copilot, copy the JSON file for the new dialog from the bot project folder to the dialogs folder in the Copilot GitHub repository.
15. Open the **[URL]** file in the Copilot GitHub repository and add a new trigger for the new intent, such as:
```
{
"$kind": "[URL]",
"intent": "showCalendar",
"actions": [
{
"$kind": "[URL]",
"dialog": "ShowCalendarDialog"
}
]
}
```
16. Save the file and redeploy Copilot to Azure using the PowerShell scripts in the deploymentScripts folder.
17. Test Copilot in the web chat or Teams and see how it handles the new intent and dialog.

