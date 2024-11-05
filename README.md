Azure AI Labs - Language Detection (Lab 1) and Image Analysis (Lab 2)
This repository contains two labs that utilize Azure's Cognitive Services APIs to perform language detection and image analysis. Each lab demonstrates both REST API and SDK client implementations to interact with Azure's Text Analytics and Computer Vision services.

Prerequisites
Azure Subscription: Ensure you have an Azure account with access to Cognitive Services.
API Key and Endpoint: Set up a Cognitive Services resource in Azure, and copy your API key and endpoint.
Setup Instructions
Clone the repository and navigate to the project directory.

Install the required packages with the following commands:


pip install python-dotenv
pip install azure-ai-textanalytics
pip install azure-ai-vision
pip install azure-core
pip install requests
pip install matplotlib
pip install pillow

Create an .env file in the project root, and add your Azure API endpoint and key as follows (replace with your values):

AI_SERVICE_ENDPOINT="https://your-azure-endpoint.cognitiveservices.azure.com/"
AI_SERVICE_KEY="your-api-key"

Lab 1: Language Detection
In Lab 1, you’ll implement a language detection tool that uses Azure's Text Analytics API to identify the language of a text input. This lab includes two implementations: a REST API-based client and an SDK client.

Instructions
REST API Client: Run lab1_rest_client.py. This script will prompt you to enter text, and it will detect the language using the REST API method until you type "quit".

python lab1_rest_client.py

SDK Client: Run lab1_sdk_client.py for the SDK client implementation. This script also prompts you to enter text and detects the language using Azure's Text Analytics SDK.

python lab1_sdk_client.py

Lab 1 Files
lab1_rest_client.py: Implements language detection using REST API.
lab1_sdk_client.py: Implements language detection using the Azure SDK client.

Features in Lab 1
Detects language from text input.
Supports continuous input until "quit" is entered.
Provides language name based on Text Analytics API results.


Lab 2: Image Analysis and Background Removal .
In Lab 2, you’ll analyze images to extract captions, tags, objects, and people using Azure’s Computer Vision API. This lab also includes a feature to remove image backgrounds.

Instructions
Run Image Analysis: Run lab2_image_analysis.py to analyze an image using the SDK client. By default, it analyzes the image images/street.jpg, but you can specify a different image path as an argument.

python lab2_image_analysis.py [image_path]

Output Files: After running the analysis, you will see results saved as annotated images, including detected objects, people, and a version with the background removed.

Lab 2 Files
lab2_image_analysis.py: Implements image analysis with the SDK client and background removal using the REST API.
images/street.jpg: Sample image used for testing image analysis.

Features in Lab 2
Caption Generation: Describes the content of the image.
Tags Extraction: Lists tags based on the image content.
Object and People Detection: Detects objects and people in the image and draws bounding boxes.
Background Removal: Removes background or generates a foreground matte for the image.

Output Files
objects.jpg: Annotated image showing detected objects.
people.jpg: Annotated image showing detected people.
background.png: Image with background removed.
