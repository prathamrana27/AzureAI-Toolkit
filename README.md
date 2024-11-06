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


Lab-03: Text Extraction and Analysis Using Azure AI Vision
Overview
This project, Lab-03, demonstrates the use of Azure's AI Vision services to read and analyze text from images. It includes a Python script that connects to Azure's Image Analysis API, allowing users to extract text and overlay detected text with bounding polygons on the original image.

Prerequisites
To run this project, you need:

A valid Azure account with access to Azure AI Vision services.
An Azure API endpoint and API key for the Image Analysis service.
Python 3.x installed on your machine.
Required Python packages:
dotenv for loading environment variables
os for file handling
Pillow for image manipulation
matplotlib for displaying images
azure-ai-vision for the Azure AI Vision client and model definitions
azure-core for Azure key credential management
Setup
Clone the repository (or download the project files).

Install the dependencies by running:

pip install -r requirements.txt

Set up environment variables:

Create a .env file in the root directory.
Add your Azure API endpoint and API key to the .env file:
makefile

AI_SERVICE_ENDPOINT=your_endpoint_here
AI_SERVICE_KEY=your_key_here
Add Images:

Place the images you want to analyze (e.g., Lincoln.jpg and Note.jpg) inside an images folder in the project directory.
Usage
Run the script by executing:

python lab-03.py
Select an option from the menu:

Option 1: Use the Read API to extract text from Lincoln.jpg.
Option 2: Extract handwriting from Note.jpg.
Any other key to exit.
View Output:

The program displays detected text in the console and overlays bounding polygons on the text in the image.
The annotated image is saved as text.jpg in the project directory.
Code Structure
main(): Initializes the Azure AI Vision client and provides a command-line menu for selecting analysis options.
GetTextRead(image_file): Reads and analyzes the specified image file for text, then overlays detected text with bounding polygons on the image.
Example
After running the script, you should see console output with the extracted text, bounding polygons, and confidence scores. The text.jpg output file will display the annotated image.

Troubleshooting
Ensure the .env file is correctly configured with your Azure endpoint and key.
Verify the required Python packages are installed.
