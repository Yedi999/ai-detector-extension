# ai-detector-extension
AI Content Detector for school platform
# AI Content Detector for Blackboard

A browser extension that helps instructors detect AI-generated content in student submissions on Blackboard Learning Management System.

## Features

- Automatically detects when viewing student submissions in Blackboard
- Analyzes text content for signs of AI generation (using GPTZero API)
- Provides probability scores and detailed analysis
- Monitors clipboard activity during tests to detect copy/paste behavior
- Tracks tab switching during assessments
- Allows manual analysis of any text

## Development Status

This extension is currently in early development (v0.1.0).

## Setup Instructions

### Prerequisites

- Node.js and npm
- A GPTZero API key (free tier available at [gptzero.me](https://gptzero.me/))

### Installation for Development

1. Clone this repository:
```
git clone https://github.com/yourusername/ai-detector-extension.git
cd ai-detector-extension
```

2. Install dependencies:
```
npm install
```

3. Run the extension in development mode:
```
npm start
```

This will open Firefox with the extension loaded. To load in Chrome:
```
npm start -- -t chromium
```

### Building for Production

To create a distributable package:
```
npm run package
```

This will create a zip file in the `dist` directory that can be uploaded to browser extension stores.

## Configuration

After installing the extension:

1. Click the extension icon in your browser toolbar
2. Click "Open Settings"
3. Enter your GPTZero API key
4. Adjust detection thresholds and other settings as needed
5. Click "Save Settings"

## Usage

### For Assignments

1. Navigate to a student submission in Blackboard
2. The extension will automatically add "Detect AI Content" buttons next to submission text
3. Click the button to analyze the content
4. View the detailed results and probability score

### For Tests

1. Enable the extension before administering an online test
2. The extension will monitor for suspicious activities like:
   - Pasting AI-generated content
   - Switching tabs during the assessment
3. View the reports section to see flagged activities

### Manual Analysis

1. Click the extension icon in your browser toolbar
2. Click "Analyze Text Manually"
3. Paste the text you want to analyze
4. Click "Analyze" to see the results

## Privacy & Ethics

This extension is designed to be used ethically and responsibly:

- No student data is stored outside the browser extension
- API requests to GPTZero only include the text being analyzed
- The extension does not report student activity to any external service
- False positives are possible - instructor judgment is still required

## License

This project is licensed under the MIT License - see the LICENSE file for details.
