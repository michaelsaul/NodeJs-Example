# NodejsSpeechTranslateApp

The sample code is designed to illustrate the 2 methods supported in the Microsoft Translater API.

1. calling /languages to get the list of supported languages for speech, text and text to speech.
2. calling /speech/translate to get the recognition and translation of an audio file. The audio file is in PCM 16bit, 16kHz mono WAV format (with header)

## Instructions
### Setup Speech Translation API in Azure
You will need to create a Microsoft Translator Speech API service in Microsoft Azure.

1. Sign up for a Microsoft Azure account at [http://azure.microsoft.com] (http://azure.microsoft.com)
2. After you have an account go to [http://portal.azure.com] (http://portal.azure.com)
3. Select the + **New** option
4. Select **Intelligence** from the list of services
5. Select **Cognitive Services APIs**
6. Select **Translater Speech API** from the **API Type** option
7. In the **Pricing Tier**, select the pricing tier that fits your needs
8. Fill out the rest of the for and select **Create**
9. Go to **All resources** and select the Microsoft Translator Speech API you just created
10. Go to the **Keys** option and make a note of **KEY 1**

### Configure and Run the Sample Application
1. Clone this repository to your development machine
2. Change to the project directory and execute "npm install"
3. Edit app.js and enter your Azure Cognitive Services Speech Translater Speech API Key from step 10 above.
```
var azureApiKey = '[Azure Cognitive Services Translator Speech API Key]';
```
3. Run by executing "node app.js"

If you want to change the audio file, simply change the line 
var file = 'helloworld.wav';

## Dependencies
request, stream-buffers, websocket

## More Information
Speech API documentation can be [found here.] (https://docs.microsofttranslator.com/)
This app posts translations to a webservice. You will need a website to post to, or change the app to post locally to the UIWebView.
