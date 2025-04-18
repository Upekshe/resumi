# resumi

A dynamic, browser-based CV/resume generator that transforms JSON data into beautifully formatted, printable documents with live editing and preview capabilities.

## Table of Contents
- [Features](#-features)
- [Quick Start](#-quick-start)
- [Data Format](#-data-format)
- [Usage Guide](#-usage-guide)
  - [Editor Mode](#1-editor-mode)
  - [Preview Mode](#2-preview-mode)
  - [Edit Mode](#3-edit-mode)
  - [URL Parameters](#4-url-parameters)
- [Printing Instructions](#-printing-instructions)
- [Technical Details](#-technical-details)
- [License](#-license)

## ✨ Features

- **JSON-powered CVs** - Define your resume content in a simple, structured JSON format
- **Multiple Input Methods**:
  - Direct JSON editing with syntax highlighting
  - URL parameter loading (?data=encoded_json)
  - GitHub Gist integration (?gist=username)
- **Real-time Preview**:
  - Accurate A4 page simulation (210×297mm)
  - 1" (25.4mm) top/bottom margins
  - 0.8" (20.32mm) side margins
  - Automatic multi-page content flow
- **Professional Styling**:
  - Times New Roman typography
  - Optimized section spacing
  - Print-friendly layout
- **Interactive Tools**:
  - JSON validator with error highlighting
  - One-click beautifier
  - Toggle between edit/preview modes

## 🚀 Quick Start

1. **Download** the standalone HTML file:
   ```bash
   wget https://example.com/cv-generator.html
   ```

2. **Open** in any modern browser:
   ```bash
   open cv-generator.html  # Or double-click the file
   ```

3. **Choose your input method**:
   - Paste JSON directly into the editor
   - Load via URL: `cv-generator.html?data=URL_ENCODED_JSON`
   - Load from GitHub: `cv-generator.html?gist=yourusername`

## 📋 Data Format

Your CV data should follow this JSON structure:

```json
{
  "header": {
    "name": "Your Full Name",
    "email": "your.email@example.com",
    "phone": "+1 (123) 456-7890",
    "linkedin": "linkedin.com/in/yourprofile"
  },
  "education": [
    {
      "institution": "University Name",
      "years": "2015-2019",
      "degree": "Degree Earned",
      "details": [
        "GPA: 3.8",
        "Honors: Magna Cum Laude",
        "Thesis: 'Advanced Topic Research'"
      ]
    }
  ],
  "experience": [
    {
      "company": "Employer Name",
      "years": "2020-Present",
      "title": "Job Title",
      "details": [
        "Led cross-functional team of 5 developers",
        "Implemented new CI/CD pipeline",
        "Reduced server costs by 30%"
      ]
    }
  ],
  "volunteer": [
    {
      "organization": "Nonprofit Name",
      "years": "2018-2020",
      "role": "Volunteer Position",
      "location": "City, Country"
    }
  ]
}
```

## 🖥️ Usage Guide

### 1. Editor Mode

- Paste your JSON into the text area
- Use the **✨ Beautify** button to format your JSON
- Errors appear in real-time with explanations
- Click **Generate CV** when ready

### 2. Preview Mode

- Click **👀 Preview** to see print layout
- Scroll through paginated A4 pages
- Dashed borders indicate margin boundaries
- Click **❌ Close Preview** to return

### 3. Edit Mode
- Click **✏️ Edit Data** on any generated CV
- Modifies the current CV while preserving structure
- Changes appear immediately after regeneration

### 4. URL Parameters

**Load from encoded JSON**:
```
cv-generator.html?data=%7B%22header%22%3A%7B%22name%22%3A%22...
```

**Load from GitHub Gist**:
```
cv-generator.html?gist=yourusername
```
*(Requires public gist named "resume-data.json")*

## 🖨️ Printing Instructions

For perfect physical copies:

1. Open the **Preview Mode**
2. Use browser print (Ctrl/Cmd + P)
3. Configure settings:
   - **Paper Size**: A4
   - **Margins**: None (or Default)
   - **Scale**: 100%
   - **Background Graphics**: Enabled


## 🛠️ Technical Details

**Browser Support**:
- Chrome, Firefox, Edge, Safari (latest versions)

**Dependencies**:
- None (100% vanilla HTML/CSS/JS)

**Print Features**:
- CSS `@page` rules for precise formatting
- Media queries for print-specific styling
- Automatic page breaks with `page-break-inside: avoid`

**Performance**:
- Client-side rendering (no server needed)
- Efficient DOM updates
- Minimal memory usage

## 📜 License

MIT License

**Note**: Always sanitize user input when using URL parameters in production environments.

---

💡 **Pro Tip**: Use [JSONLint](https://jsonlint.com/) to validate your JSON before pasting!



