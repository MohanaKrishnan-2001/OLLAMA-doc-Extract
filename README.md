# OLLAMA-doc-Extract
AI-powered document extractor for Indian government documents. Upload photos of AADHAAR, PAN, DL &amp; RC - get structured JSON data instantly! Built with Python, OLLAMA &amp; Qwen2.5VL. 100% local processing.

# 🔍 AI Document Extractor

> Transform your document processing workflow with the power of AI! Upload photos of Indian government documents and watch as our smart AI reads and extracts all the information instantly.

![Document Extractor Demo](https://img.shields.io/badge/Status-Active-brightgreen) ![Python](https://img.shields.io/badge/Python-3.8%2B-blue) ![OLLAMA](https://img.shields.io/badge/OLLAMA-Powered-orange) ![Dash](https://img.shields.io/badge/Framework-Dash-lightblue)

## 🎯 What Does This Do?

Imagine having a super-smart assistant that never gets tired of reading documents! This application uses AI to automatically extract information from photos of Indian government documents like AADHAAR cards, PAN cards, driving licenses, and vehicle registration certificates.

### ✨ Key Features

- **🤖 AI-Powered**: Uses advanced Qwen 2.5VL vision model through OLLAMA
- **📱 Drag & Drop Interface**: Simply drag your document photos and let AI do the work
- **🎨 Beautiful UI**: Professional design with smooth animations and real-time feedback
- **📊 Smart Statistics**: Track how many documents you've processed
- **💾 Auto-Save**: Results automatically saved as JSON files
- **🔒 100% Private**: Everything runs locally on your computer - no data leaves your machine

## 🚀 Quick Start

### What You'll Need

Before we begin, make sure you have:
- A computer (Windows, Mac, or Linux)
- Python 3.8 or newer
- About 10 minutes to set everything up

### Step 1: Install OLLAMA

OLLAMA is the AI engine that powers our document reader.

**For Windows:**
1. Go to [ollama.ai](https://ollama.ai)
2. Download and install OLLAMA
3. Open Command Prompt and run: `ollama run qwen2.5vl:7b`

**For Mac/Linux/Windows:**
```bash
curl -fsSL https://ollama.ai/install.sh | sh
ollama run qwen2.5vl:7b
```

*Note: The first time will download about 4GB of AI model - grab a coffee! ☕*

### Step 2: Install Python Dependencies

```bash
pip install dash dash-bootstrap-components opencv-python pillow requests numpy
```

### Step 3: Run the App

```bash
python app.py
# or
python app.ipynb
```

Open your browser and go to: `http://127.0.0.1:7050`

That's it! You're ready to extract documents! 🎉

## 📖 How to Use

### The Easy Way:

1. **Start the App**: Run `python app.py` and open `http://127.0.0.1:7050`

2. **Upload a Document**: 
   - Drag and drop a photo of your document
   - Or click "Select Files" to browse

3. **Process**: Click the big blue "🚀 Process Document" button

4. **See Results**: Watch the AI work its magic and see all extracted information!

5. **Find Your Data**: Results are automatically saved in the `JSON_OP` folder

### What Documents Work?

| Document Type | What We Extract |
|---------------|-----------------|
| 🆔 **AADHAAR Card** | AADHAAR number, name, DOB, address, gender |
| 🏷️ **PAN Card** | PAN number, name, father's name, DOB |
| 🚘 **Driving License** | License number, name, validity, address, blood group |
| 🚗 **RC Book** | Registration number, owner, vehicle details, engine number |

## 🎨 What Makes This Special?

### Smart Image Processing
- Automatically resizes and enhances your photos
- Removes noise and improves text clarity
- Works with photos taken from phones or scanners

### Beautiful Interface
- Professional design with calming colors
- Smooth animations that make processing fun
- Real-time progress updates
- Statistics dashboard to track your work

### Reliable AI Brain
- Uses Qwen 2.5VL - one of the most advanced vision models
- Validates document authenticity
- Provides confidence scores for extractions
- Handles errors gracefully with helpful messages

## ⚙️ Configuration

You can customize the app by editing these settings in `app.py`:

```python
# AI Model Configuration
MODEL_NAME = "qwen2.5vl:7b"          # AI model to use
OLLAMA_URL = "http://localhost:11434"  # OLLAMA server address

# File Storage
OUTPUT_DIRECTORY = "JSON_OP"          # Where to save results
```

## 🔧 Troubleshooting

### Common Issues & Solutions

**Problem**: "Connection refused" error
- **Solution**: Make sure OLLAMA is running (`ollama serve` in terminal)

**Problem**: "Model not found" error  
- **Solution**: Download the model first (`ollama pull qwen2.5vl:7b`)

**Problem**: Slow processing
- **Solution**: The AI model needs good CPU/GPU. First run is always slower.

**Problem**: Poor extraction quality
- **Solution**: Try taking a clearer photo with good lighting

### Need Help?

1. Check that OLLAMA is running: `http://localhost:11434` should show a page
2. Verify the model is installed: `ollama list` should show `qwen2.5vl:7b`
3. Make sure all Python packages are installed: `pip install -r requirements.txt`

## 📁 Project Structure

```
ai-document-extractor/
│
├── app.py                 # Main application file
├── app.ipynb             # Jupyter notebook version
├── README.md             # This file!
├── requirements.txt      # Python dependencies
└── JSON_OP/             # Where extracted data is saved
```

---

<p align="center">
  <strong>Made with ❤️ and lots of ☕ by developers who got tired of typing document information manually!</strong>
</p>
