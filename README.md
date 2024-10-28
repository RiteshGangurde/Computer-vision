
# Analyze Images with Azure AI Computer Vision

Azure AI Vision provides artificial intelligence capabilities to analyze visual input by analyzing images. The service includes models for common computer vision tasks, such as generating captions, identifying common objects, detecting landmarks, and moderating content.

## Clone the Repository for This Course

1. Open Visual Studio Code.
2. Use the Git: Clone command to clone the [AI-102-AIEngineer repository](https://github.com/MicrosoftLearning/AI-102-AIEngineer).
3. Open the cloned folder in Visual Studio Code.

## Provision an Azure AI Services Resource

1. Open the Azure portal at [https://portal.azure.com](https://portal.azure.com).
2. Search for "Azure AI Services" and create an Azure AI multi-service account with the following settings:
   - **Subscription**: Your Azure subscription.
   - **Resource group**: Choose or create a resource group.
   - **Region**: Select an available region.
   - **Name**: Enter a unique name.
   - **Pricing tier**: Standard S0.

3. After deployment, access the Keys and Endpoint page to retrieve necessary credentials.

## Prepare to Use the Azure AI Vision SDK

1. In Visual Studio Code, navigate to the appropriate language folder (`C#` or `Python`).
2. Open an integrated terminal in the `image-analysis` folder.
3. Install the Azure AI Vision SDK:
   
   - **C#**:
     ```bash
     dotnet add package Microsoft.Azure.CognitiveServices.Vision.ComputerVision --version 6.0.0
     ```

   - **Python**:
     ```bash
     pip install azure-cognitiveservices-vision-computervision==0.7.0
     ```
   - Create a `.env` file in the root directory.
   - Add your Azure Vision API credentials:

    ```env
    AI_SERVICE_ENDPOINT=your_azure_endpoint
    AI_SERVICE_KEY=your_azure_key
    ```
    - Replace `your_azure_endpoint` and `your_azure_key` with your actual Azure

##Output

-Original Image
![street](https://github.com/user-attachments/assets/3cc765b7-4737-465a-8926-63ff7c3f65b5)

 
-Modified(Analyzed) Screenshot
![Screenshot 2024-10-28 105001](https://github.com/user-attachments/assets/14cc21f6-c73b-4d64-9f76-91e23f33ad57)

 



## Analyze Images

1. Authenticate the Azure AI Vision client using your credentials.
2. Specify features to retrieve, such as captions, tags, and categories.
3. Implement image analysis functions in the code file.
4. Run the program with sample images and observe the output captions, tags, and detected objects.

## Additional Features

- **Thumbnail Generation**: Crop and create a smaller version of the image focusing on the main subject.
- **Moderation Ratings**: Detect and classify images as adult, racy, or gory based on content.
- **Brands and Objects Detection**: Identify brands and specific objects with bounding boxes.

@princyi
