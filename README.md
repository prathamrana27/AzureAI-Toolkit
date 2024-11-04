# AzureAI-Toolkit
-----------------
Language Detection Application
This application detects the language of any text you enter using Azure's Text Analytics API. It includes two ways to run the code:

Prerequisites
--------------
To run this project, you’ll need:

Python 3.6 or higher installed on your computer.
Azure Account with an Azure Text Analytics resource (to get an API endpoint and key).
A .env file to securely store your Azure endpoint and key.
Setting Up the .env File
In the project folder, create a file named .env.

Inside this file, add the following lines, replacing the placeholders with your actual Azure Text Analytics endpoint and key:

AI_SERVICE_ENDPOINT="https://your-azure-endpoint.cognitiveservices.azure.com/"
AI_SERVICE_KEY="your_azure_key"

(Make sure to replace your-azure-endpoint and your_azure_key with your actual Azure information.)

Installing Required Packages
Open a terminal (or command prompt) in the project folder.
Run the following command to install the necessary libraries:
---------------------------------------------------------------
| pip install python-dotenv azure-core azure-ai-textanalytics |
---------------------------------------------------------------
