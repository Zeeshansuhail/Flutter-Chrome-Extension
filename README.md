# Chrome Extension with Flutter, OpenAI & LangChain: AI-Powered Summarization
An AI-powered Chrome extension that automatically summarizes the content of your current tab. Built by combining the power of Flutter, OpenAI, and LangChain. 

## Features: 
* Chrome extension with one popup view build with Flutter (using [atomsbox.com](https://atomsbox.com))
* Dart JS interop to use the [chrome JS library](https://developer.chrome.com/docs/extensions/reference/)
* HTTP client to send requests to a Cloud Function on Google Cloud Platform
* Python script to scrape the content of the current tab (BeautifulSoup) and to summarize the content (OpenAI + LangChain)

![diagram](assets/atomsbox_chrome_extension_flutter_openai_langchain.png)

## Prerequisites
Before you start, make sure you have the following:

* [OpenAI API Key](https://platform.openai.com/account/api-keys)
* [Google Cloud Platform account](https://console.cloud.google.com/)


## Getting Started

Step 1: Setting up the project:
Open your terminal/command prompt and create a new Flutter project by running:
```bash
flutter create my_chrome_extension
```

Step 2: Change your working directory to the newly created project folder and open it in a Visual Studio Code:
```bash
cd my_chrome_extension
```

Step 3: Prepare the Flutter UI ([video tutorial](https://colab.research.google.com/drive/1FSsmOOee0GeFUe6u260bmSWhNpAvfaPO?authuser=2#scrollTo=Gyd-Uifiev4i))


Step 4: Deploy a Cloud Function ([video tutorial](https://colab.research.google.com/drive/1FSsmOOee0GeFUe6u260bmSWhNpAvfaPO?authuser=2#scrollTo=Gyd-Uifiev4i), [python code](https://colab.research.google.com/drive/1FSsmOOee0GeFUe6u260bmSWhNpAvfaPO?authuser=2#scrollTo=Gyd-Uifiev4i))


Step 4: Build the Chrome extension
```bash
flutter build web --web-renderer html --csp
```


Step 5: Loading and testing the extension in Chrome
* Open Chrome and go to chrome://extensions/.
* Enable "Developer mode" by toggling the switch in the top-right corner.
* Click "Load unpacked" and select the build/web folder from your project directory.

Your extension should now appear in the list of installed extensions, and you can test its functionality.
