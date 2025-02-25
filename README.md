# CodeGPT API Chatbot with Gradio  

## Overview  
This project is a **Gradio-based chatbot** that interacts with **CodeGPT** using a REST API. It sends prompts to the **local CodeGPT model running on port 11434** and returns AI-generated responses.  

## Features  
- 💬 **Chat with CodeGPT using Gradio**  
- 🔄 **Maintains chat history for better context**  
- ⚡ **Simple and fast API-based interaction**  
- 🚀 **Runs locally without external dependencies**  

## Prerequisites  
- Python **3.8+**  
- **CodeGPT API** running on `localhost:11434`  
- Required dependencies installed  

## Installation  

### 1️⃣ Install Dependencies  
Run the following command to install required Python packages:  

```sh
pip install requests gradio
```

### 2️⃣ Run CodeGPT API  
Ensure your **CodeGPT API** is running at `http://localhost:11434/api/generate`. 

## Prerequisites  
- **Ollama** installed ([Download here](https://ollama.com/download))  
- **Python 3.8+** installed (for API testing)  

## Installation  

### 2.1 Install Ollama  
Run the following command to install Ollama:  

```sh
curl -fsSL https://ollama.com/install.sh | sh
For Windows, download and install from https://ollama.com/download.
```

### 2.2 Download CodeLlama Model
Pull a CodeLlama model (e.g., 7B version):

```sh

ollama pull codellama:7b
```
### 2.3 Create a Custom Model (modelfile)
Create a new file named modelfile and add:

```txt

FROM codellama


## Set the Temperature
PARAMETER temperature 1

## Set the system prompt
SYSTEM """
You are a code teaching assistant named CodeGPT, created by HimanshU. Answer all the coding-related questions."""
```
### 2.4 Build the Custom Model
Run the following command:

```sh

ollama create codegpt -f modelfile
```
### 2.5 Start the API Server
Run:

```sh

ollama serve
```
This will start the API at http://localhost:11434/api/generate.

## Usage  

### 1️⃣ Start the Gradio Chatbot  
Run the Python script:  

```sh
python app.py
```

### 2️⃣ Interact with the Chatbot  
- Enter a **prompt** in the Gradio interface.  
- Click **Submit** to get a response.  
- The chat **remembers history** for better context.  

## Project Structure  

```
📂 codeGPT-chatbot
│── app.py              # Main chatbot script
│── README.md           # Project documentation
│── requirements.txt    # Dependencies
```

## Future Enhancements  
- ✅ Add **streaming responses** for real-time chat  
- ✅ Implement **custom models** for different use cases  
- ✅ Improve **error handling** for API failures  

## License  
This project is **open-source** and available under the **MIT License**.  
