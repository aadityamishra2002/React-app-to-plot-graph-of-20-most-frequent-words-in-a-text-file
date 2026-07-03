# Word Frequency Visualizer 📊

> Analyze any text and visualize the top 20 most common words with an interactive bar chart. 
> Built with React and Recharts for fast, intuitive text analysis.

🔗 **[Live Demo](https://marvelous-piroshki-85bf31.netlify.app/)** | 💻 [GitHub](https://github.com/aadityamishra2002/word-frequency-visualizer)

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 📤 **Text Input** | Upload text files or paste text directly |
| 📊 **Word Frequency Chart** | Interactive bar chart of top 20 words |
| 🎨 **Responsive Design** | Works on desktop, tablet, mobile |
| 📥 **Export CSV** | Download results as CSV for further analysis |
| ⚡ **Real-time Processing** | Instant results as you paste or upload |
| 🎯 **Stop Words Filtering** | Optional: remove common words (the, and, is, etc.) |

---

## 🎯 Use Cases

- **Content Analysis:** Identify key themes in blog posts, articles, speeches
- **SEO Optimization:** Find your most-used keywords and optimize
- **Text Mining:** Analyze surveys, feedback, social media posts
- **Academic Research:** Analyze corpus of texts for patterns
- **Document Review:** Quickly understand what a document is about

---

## 🛠️ Tech Stack

| Technology | Purpose |
|-----------|---------|
| **React** | UI framework, component state management |
| **Recharts** | Beautiful, responsive charting library |
| **Axios** | Fetch text from URLs |
| **Netlify** | Deployment, hosting |
| **Create React App** | Build tooling |

---

## 🚀 Getting Started

### Prerequisites

- Node.js 14+ 
- npm or yarn

### Installation

```bash
# Clone repository
git clone https://github.com/aadityamishra2002/word-frequency-visualizer.git
cd word-frequency-visualizer

# Install dependencies
npm install

# Start development server
npm start

# Open browser
# Navigate to http://localhost:3000
```

### Build for Production

```bash
npm run build
# Output: build/ directory (ready to deploy)
```

---

## 📝 How to Use

### Method 1: Paste Text

1. Copy text to clipboard
2. Paste into the textarea
3. Click "Analyze"
4. View chart and export CSV

### Method 2: Upload File

1. Click "Upload Text File"
2. Select a `.txt` file
3. Processing begins automatically
4. View results

### Method 3: Fetch from URL

1. Enter URL to a text document
2. Click "Fetch & Analyze"
3. App downloads and analyzes text
4. View results

---

## 📊 Example Output

**Input Text:**
```
"The quick brown fox jumps over the lazy dog. The fox is quick. 
The dog is lazy but the fox is very quick and clever."
```

**Word Frequency Results:**
```
| Word   | Frequency |
|--------|-----------|
| the    | 4         |
| fox    | 3         |
| quick  | 3         |
| lazy   | 2         |
| is     | 2         |
| dog    | 2         |
| over   | 1         |
| jumps  | 1         |
| brown  | 1         |
| clever | 1         |
```

**Visualization:** Interactive bar chart with Recharts

---

## 💡 What I Learned

### 1. **Text Processing**
- Tokenization: Split text into words
- Normalization: Convert to lowercase, remove punctuation
- Stop words: Common words that add little value

### 2. **React Patterns**
- State management with `useState`
- Handling file uploads with `<input type="file">`
- Real-time filtering with useEffect

### 3. **Data Visualization**
- Recharts for responsive, beautiful charts
- D3 concepts simplified
- Interactive tooltips and legends

### 4. **Full-Stack Development**
- Frontend (React components)
- Backend considerations (CORS, file handling)
- Deployment (Netlify, build optimization)

---

## 📈 Optimization Tips

### For Large Files (>1MB)

```javascript
// Chunk processing instead of loading all at once
const CHUNK_SIZE = 10000;

for (let i = 0; i < text.length; i += CHUNK_SIZE) {
  const chunk = text.slice(i, i + CHUNK_SIZE);
  processChunk(chunk);
}
```

### For Real-time Updates

```javascript
// Debounce analysis to avoid excessive re-renders
const debouncedAnalyze = useCallback(
  debounce((text) => analyzeText(text), 500),
  []
);
```

### For Mobile Performance

```javascript
// Limit chart size on small screens
const isSmallScreen = window.innerWidth < 768;
const chartHeight = isSmallScreen ? 300 : 500;
```

---

## 🔄 Project Structure

```
word-frequency-visualizer/
├── src/
│   ├── components/
│   │   ├── TextInput.jsx      # Text input/upload component
│   │   ├── Chart.jsx           # Recharts visualization
│   │   └── Results.jsx         # Results display + CSV export
│   ├── utils/
│   │   ├── analyzeText.js      # Word frequency logic
│   │   └── stopWords.js        # Common stop words list
│   ├── App.jsx                 # Main app component
│   └── App.css                 # Styling
├── public/
│   └── index.html              # HTML entry point
├── package.json                # Dependencies
└── README.md                   # This file
```

---

## 🔜 Potential Improvements

- [ ] **N-gram analysis** — Analyze word pairs and phrases (e.g., "machine learning")
- [ ] **Language detection** — Handle multiple languages, different stop word lists
- [ ] **Sentiment analysis** — Color-code words by sentiment (positive/negative)
- [ ] **Word cloud** — Alternative visualization (word size = frequency)
- [ ] **Comparison mode** — Compare word frequency across multiple texts
- [ ] **Historical tracking** — See how word frequency changes over time
- [ ] **API endpoint** — RESTful API for programmatic access

---

## 📧 Questions?

**Email:** aadityamishra1063@gmail.com  
**LinkedIn:** [linkedin.com/in/adityamishra2002](https://www.linkedin.com/in/adityamishra2002)  
**Live Demo:** [Try it now](https://marvelous-piroshki-85bf31.netlify.app/)

---

**Last Updated:** July 2026 | Active Project
