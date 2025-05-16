
# 📄 Decked Out PDF/PPTX Analyzer

An AI‑powered Streamlit app that lets you upload PDF or PowerPoint files and instantly generate concise, high‑value notes in three styles—Official, English, or Hinglish—using Google’s Gemini API. You can also chat interactively about your document’s contents and download your notes as Markdown.

---

## 🚀 Features

- **Multi‑Format Support**: Upload `.pdf` or `.pptx` documents.  
- **Three Note Styles**  
  - **Official Notes**: Formal, structured summaries with technical precision  
  - **English Notes**: Simple, conversational plain‑English takeaways  
  - **Hinglish Notes**: Mixed Hindi‑English (Roman script) for bilingual audiences  
- **AI‑Driven Summaries**: Powered by Google Generative AI (Gemini models)  
- **Document Preview**: See a snapshot of the first page of your PDF  
- **Interactive Chat**: Ask follow‑up questions about your generated notes  
- **Markdown Export**: Download notes as `.md` files for easy sharing or editing  

---

## 📦 Requirements

### Python dependencies

```text
streamlit
pdf2image
PyPDF2
google-generativeai
python-dotenv
pillow
python-pptx
````

Install with:

```bash
pip install -r requirements.txt
```

### System dependencies

* **Poppler** (required by `pdf2image` for PDF→image conversion)

  * **macOS**:

    ```bash
    brew install poppler
    ```
  * **Ubuntu/Debian**:

    ```bash
    sudo apt-get install poppler-utils
    ```
  * **Windows**:

  1. Download Poppler binaries from
     [https://github.com/oschwartz10612/poppler-windows/releases](https://github.com/oschwartz10612/poppler-windows/releases)
  2. Extract and add the `bin/` folder to your `PATH`

---

## 🔧 Setup & Configuration

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/decked-out-pdf-analyzer.git
   cd decked-out-pdf-analyzer
   ```

2. **Create a `.env` file** in the project root containing your API key and model choice:

   ```env
   GOOGLE_API_KEY=your_google_generative_ai_key
   MODEL=gemini-2.0-flash   # or gemini-2.0-pro
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application**

   ```bash
   streamlit run app.py
   ```

   The app will be available at `http://localhost:8501/`.

---

## 📝 Usage

1. **Upload** your PDF or PPTX file.
2. **Select** a notes style: Official, English, or Hinglish.
3. **Click** “Generate Notes” to let Gemini analyze and summarize.
4. **View** the AI‑generated notes and **download** them as Markdown.
5. **Switch** to the **Chat** tab to ask questions about your notes.

---

## ⚙️ Customization

* **Change Gemini Model**: Edit the `MODEL` value in `.env`.
* **PDF Extraction Fallback**: If `pdf2image` fails, PyPDF2 will attempt text extraction.
* **Debug Mode**: Toggle `show_debug = True` in `app.py` for extra logging.

---

## 🛠️ Troubleshooting

* **“Google API Key not found”**

  * Ensure `.env` is present and Streamlit has been restarted.
* **Blank or garbled PDF text**

  * Verify Poppler is installed and on your `PATH`.
  * Try converting the PDF to a simpler format.
* **Dependency installation errors**

  * Use a clean virtual environment.
  * Upgrade pip:

    ```bash
    pip install --upgrade pip
    ```

---


## 📄 License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.
