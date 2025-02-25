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
