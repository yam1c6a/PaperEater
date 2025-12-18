# PaperEater

PaperEater is a Tauri-based desktop application that fetches the **latest 2,000 computer science papers from arXiv** and automatically filters them to show only papers related to current AI trends, such as:

**AI / AGI / ASI / LLM / OpenAI / ChatGPT / Claude / Gemini / Mistral / Sora**, and more.

All features run locally in a desktop app.

---

## Features

PaperEater provides the following functionality:

- Fetching the latest paper list from arXiv  
- Automatic trend-based filtering  
- PDF download with progress indicator  
- Optional paper title translation

---

## How It Works

### 1. Fetch the latest 2,000 papers from the `cs` category

PaperEater automatically fetches data from:

```
https://arxiv.org/list/cs/recent?show=2000
```

---

### 2. Automatic filtering using AI-related keywords (Preset B)

Only papers containing trending AI-related terms are kept, including:

- AI / AGI / ASI / LLM / VLM / multimodal  
- OpenAI / GPT / ChatGPT / o1  
- Claude / Anthropic  
- Gemini / DeepMind  
- Mistral  
- LLaMA / Meta  
- Sora / diffusion  
- RAG / alignment  

---

### 3. PDF download with progress UI

PDF files can be downloaded directly from the app, with a visible progress indicator during download.

---

### 4. Optional title translation

#### Using a DeepL API key (Japanese title translation)

To enable automatic Japanese translation of paper titles, set your DeepL API key in `index.html`:

```js
const DEEPL_API_KEY = "YOUR_API_KEY_HERE";
```

#### Without an API key (default behavior)

- If the DeepL API key is empty, title translation is skipped.
- The application works fully without any external translation API.

---

## Development Environment

### Requirements

- Node.js 18+
- Rust (stable)
- Tauri CLI

---

## Setup

```sh
npm install
npm run tauri dev
```

---

## Build

```sh
npm run tauri build
```

Build artifacts will be generated in:

```
src-tauri/target/release/bundle/
```

---

## GitHub Actions (Automated Builds)

Running `.github/workflows/tauri-build.yml` will automatically build:

- PaperEater for Windows  
- PaperEater for macOS  

---

## Project Structure

```
PaperEater/
  index.html
  README.md
  package.json
  src-tauri/
    tauri.conf.json
```

---

## License

MIT License
