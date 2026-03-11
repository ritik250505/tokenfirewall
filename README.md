# 🔥 tokenfirewall - Control LLM Costs Easily

[![Download tokenfirewall](https://img.shields.io/badge/Download-Here-green?style=for-the-badge)](https://github.com/ritik250505/tokenfirewall)

---

## 🔍 What is tokenfirewall?

tokenfirewall helps you control costs when using language models like OpenAI or Anthropic. It acts like a gatekeeper between your app and these services. It keeps your usage within your budget. It automatically switches between providers if one fails. It works with Node.js to make sure your app does not spend too much on AI calls.

This software is designed for developers with some experience but anyone interested in controlling AI costs can follow this guide to run the program on Windows.

## ⚙️ Key Features

- **Cost control:** Stops spending once your budget is reached.  
- **Supports multiple AI providers:** Works with OpenAI, Anthropic, Gemini, and more.  
- **Automatic failover:** Switches to backup providers if one goes down.  
- **Model routing:** Sends requests to the best model based on rules you set.  
- **Token counting:** Tracks how many tokens you use to bill accurately.  
- **Built with Node.js and TypeScript:** Easy to maintain and extend.

## 💻 System Requirements

Before downloading, make sure your Windows PC meets these requirements:

- Windows 10 or later (64-bit preferred)  
- At least 4 GB of RAM  
- 500 MB free disk space for installation  
- Node.js version 14 or higher installed  
- Internet connection to download packages and connect to AI services  

If you do not have Node.js installed, visit https://nodejs.org/en/download/ and download the Windows installer.

## 🚀 Getting Started: Download and Setup

### Step 1: Download tokenfirewall

Click the big green download badge above or use this link:

[Download tokenfirewall from GitHub](https://github.com/ritik250505/tokenfirewall)

This link opens the repository page on GitHub, where you will find the latest version to download.

### Step 2: Download the latest release

1. On GitHub, click the **Releases** tab usually found near the top (next to 'Code').  
2. Choose the latest release by date or version number.  
3. Download the source code ZIP file by clicking **Source code (zip)**.  
4. Save it anywhere you can easily find it, such as your Desktop or Downloads folder.

### Step 3: Extract the files

1. Right-click the downloaded ZIP file.  
2. Select **Extract All…** and choose a folder to unzip the files, like `C:\tokenfirewall`.  
3. Click **Extract**.

### Step 4: Install Node.js packages

tokenfirewall needs packages from the internet before it will run.

1. Open **Command Prompt**: Press the Windows key, type `cmd`, then press Enter.  
2. In the command window, type:

    ```
    cd C:\tokenfirewall
    ```

    Replace `C:\tokenfirewall` with your folder path if different.

3. Type this command to install the required packages:

    ```
    npm install
    ```

4. Wait while the packages download and install. You will see many lines of text. When complete, the prompt will return.

## 🛠 How to Run tokenfirewall

1. Still in the command window, type:

    ```
    npm start
    ```

2. The program will launch and run. It will listen for requests to control AI costs.  
3. You may need to configure it with your API keys for AI providers such as OpenAI or Anthropic.

## 🔑 Setting Up API Keys

To use tokenfirewall with AI models, you must supply your API keys.

1. Obtain your API keys from your AI account dashboard:  
   - OpenAI: https://platform.openai.com/account/api-keys  
   - Anthropic: https://console.anthropic.com/api-keys  
   - Gemini and others should have similar pages.

2. In the tokenfirewall folder, find the file named `.env.example`.  
3. Make a copy of this file and rename it to `.env`.  
4. Open `.env` in a text editor (Notepad works).  
5. Add your API keys in the format:

    ```
    OPENAI_API_KEY=your_openai_key_here
    ANTHROPIC_API_KEY=your_anthropic_key_here
    ```

6. Save and close the file.

## 🔧 Configuration Overview

tokenfirewall lets you adjust settings to fit your needs. The main files to edit are:

- `.env`: Store your secret API keys.  
- `config.json`: Set budget limits, choose providers order for failover, and define model routing rules.  

Example snippet for budget:

```json
{
  "budget": 50,
  "currency": "USD",
  "providers": ["openai", "anthropic", "gemini"],
  "routingRules": [
    {
      "model": "gpt-4",
      "maxTokens": 3000,
      "provider": "openai"
    }
  ]
}
```

Save changes and restart tokenfirewall after editing these files for settings to apply.

## 📊 How It Works

tokenfirewall tracks how many tokens you use on AI calls in real-time. It stops any requests that exceed the budget. If your primary AI provider fails, it switches to the next one automatically. This keeps your apps running without extra spending.

## ⚠️ Common Issues

- **Node.js not found:** Make sure Node.js is installed and `npm` commands work.  
- **API key errors:** Double-check keys are correct and active on your AI provider account.  
- **Port conflicts:** tokenfirewall listens on a network port by default; another program may block it. Change port in `config.json` if needed.  
- **Firewall blocking:** Allow tokenfirewall through Windows Defender or other firewalls.

## 🔄 Updating tokenfirewall

To get the latest features and fixes:

1. Download the newest release from the GitHub Releases page.  
2. Replace your folder files with the new ones.  
3. Run `npm install` again to update packages if prompted.  
4. Restart tokenfirewall.

## 🖥 Help and Support

For questions or help, check the GitHub repo Issues page. You can report problems or request guidance there:

https://github.com/ritik250505/tokenfirewall/issues

---

[![Download tokenfirewall](https://img.shields.io/badge/Download-Here-green?style=for-the-badge)](https://github.com/ritik250505/tokenfirewall)