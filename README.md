# Claude-Ask

![HTML](https://img.shields.io/badge/Language-HTML-E34F26?style=for-the-badge&logo=html5&logoColor=white)

A browser-based tool that connects spreadsheet cells to Claude. Built for workflows where you're processing rows of data and want Claude to handle each one without manually copying and pasting every time.

---

## What It Does

You put a `HYPERLINK` formula in your spreadsheet that references a cell. When you click the link, the page opens with that cell's content loaded into an editable prompt window. The prompt is automatically copied to your clipboard. You click the button to open Claude.ai, paste, and send.

No API key. No backend. Nothing stored.

---

## Features

- Reads prompt content from a URL parameter
- Auto-copies to clipboard on load
- Editable before sending — you can adjust the prompt on the page
- Opens Claude.ai directly
- Nothing is logged or stored anywhere
- Hosted on GitHub Pages, no server required

---

## How It Works

```
Spreadsheet cell → HYPERLINK formula → ask.html → clipboard → Claude.ai
```

---

## Spreadsheet Formula

### Basic
```
=HYPERLINK("https://jarredward1.github.io/claude-ask/ask.html?q="&A2, "Ask Claude →")
```

### With a prompt template
```
=HYPERLINK("https://jarredward1.github.io/claude-ask/ask.html?q=Analyze this job description and identify the top skills required: "&A2, "Ask Claude →")
```

### If your cell content contains `&`
```
=HYPERLINK("https://jarredward1.github.io/claude-ask/ask.html?q="&SUBSTITUTE(A2,"&","%26"), "Ask Claude →")
```

Drag the formula down and each row gets its own link.

---

## Live Demo

👉 [jarredward1.github.io/claude-ask/ask.html?q=Hello+World](https://jarredward1.github.io/claude-ask/ask.html?q=Hello+World)

---

## Privacy

No data is collected, stored, or sent anywhere. Prompts exist only in the URL and your clipboard.

---

## 👤 Author

**Jarred Ward**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?logo=linkedin&style=for-the-badge)](https://www.linkedin.com/in/jarredward1/)
