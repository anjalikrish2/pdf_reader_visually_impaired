# Accessible PDF Reader with OCR


**Developed for**: EkStep Foundation

**A voice-controlled, accessible PDF reader with automatic text extraction for all types of documents**

---

## Overview

This is a comprehensive web-based PDF reader designed for maximum accessibility. It combines voice control, text-to-speech, and OCR (Optical Character Recognition) to make PDF documents accessible to all users, including those with visual impairments or reading difficulties. The application can read both text-based PDFs and scanned/image-based documents.

---

## Key Features

### Core Functionality
- **Universal PDF Support**: Reads both native text PDFs and scanned/image-based PDFs
- **Automatic Text Extraction**: Intelligent text extraction with fallback to OCR when needed
- **Text-to-Speech**: High-quality voice reading with customizable settings
- **Voice Commands**: Hands-free navigation and control
- **Multi-language OCR**: Supports English, Hindi, Tamil, Telugu, Kannada, Marathi, and Bengali

### Accessibility Features
- **Full keyboard navigation** with comprehensive shortcuts
- **Screen reader compatible** with ARIA labels and live regions
- **High contrast mode** support
- **Reduced motion** support for users with vestibular disorders
- **Focus indicators** for keyboard-only navigation
- **Semantic HTML** structure

### User Experience
- **Bookmarking system** for important pages
- **Page jumping** - go directly to any page number
- **Reading progress tracking** with visual highlights
- **Auto-advance** to next page when reading completes
- **Adjustable voice settings** (speed, pitch, voice selection)
- **Drag-and-drop** file upload

---

## Voice Commands

Users can control the reader hands-free with these commands:

| Command | Action |
|---------|--------|
| "Next" / "Forward" | Go to next page and start reading |
| "Back" / "Previous" | Go to previous page and start reading |
| "Stop" / "Pause" | Stop reading |
| "Start" / "Play" | Start reading current page |
| "Repeat" / "Again" | Repeat current page and start reading |
| "Bookmark" | Bookmark current page |
| "Faster" | Increase reading speed |
| "Slower" | Decrease reading speed |
| "Reprocess" | Rerun OCR on current page |
| "Go to page [number]" | Jump to specific page |

---

## Keyboard Shortcuts

| Key | Action |
|-----|--------|
| **N** | Next page |
| **B** | Previous page |
| **Space** | Play/Pause reading |
| **R** | Repeat current page |
| **M** | Add bookmark |
| **V** | Toggle voice commands |
| **O** | Reprocess page with OCR |
| **J** | Focus on page jump input |
| **T** | Test voice settings |
| **Esc** | Stop all activity |

---

## How It Works

### Document Processing Flow

1. **Upload**: User uploads a PDF file via click, drag-and-drop, or keyboard
2. **Analysis**: System extracts text from the PDF using PDF.js
3. **OCR Fallback**: If insufficient text is found, Tesseract.js OCR is automatically triggered
4. **Text Processing**: Extracted text is cleaned, formatted, and split into sentences
5. **Rendering**: Page is rendered both as canvas (visual) and text (accessible)
6. **Reading**: Text-to-speech engine reads content sentence-by-sentence with visual highlights

### OCR Technology

When a page contains images or scanned content:
- High-resolution canvas rendering (2.5x scale) for accuracy
- Tesseract.js performs optical character recognition
- Progress indicator shows OCR status
- Supports 8 Indian and international languages
- Results are cached for performance

---

## Technical Architecture

### Technologies Used

- **PDF.js** (v3.11.174) - PDF rendering and text extraction
- **Tesseract.js** (v4.1.4) - OCR processing
- **Web Speech API** - Text-to-speech synthesis
- **Web Speech Recognition API** - Voice command processing
- **HTML5 Canvas** - Page rendering
- **Modern CSS** - Responsive, accessible styling

### Browser Compatibility

**Required Features:**
- Web Speech API (for text-to-speech)
- Web Speech Recognition API (for voice commands - Chrome/Edge recommended)
- HTML5 Canvas
- ES6+ JavaScript support
- Web Workers (for PDF.js)

**Recommended Browsers:**
- Google Chrome 90+
- Microsoft Edge 90+
- Safari 14+ (limited voice recognition)
- Firefox 88+ (limited voice features)

---

## Installation & Usage

### Quick Start

1. **Download** the HTML file
2. **Open** in a modern web browser (Chrome/Edge recommended)
3. **Upload** a PDF file
4. **Click** "Start Voice Commands" or "Start Reading"
5. **Navigate** using voice, keyboard, or mouse

### No Installation Required

This is a standalone HTML file with all dependencies loaded from CDN:
- No server required
- No build process needed
- Works offline after initial load (with cached CDN resources)
- No data leaves the browser - fully private

---

## Customization Options

### Voice Settings
- **Voice Selection**: Choose from all available system voices
- **Speed**: 0.3x to 2.0x (default: 0.8x)
- **Pitch**: 0.5 to 2.0 (default: 1.0)
- **Test Voice**: Preview settings before reading

### OCR Settings
- **Language Selection**: 8 supported languages
- **Multi-language**: Combine languages (e.g., English + Hindi)
- **Reprocess Option**: Re-run OCR if initial extraction was poor

---

## Accessibility Compliance

This application follows Web Content Accessibility Guidelines (WCAG) 2.1:

### Level A Compliance
✓ Keyboard accessible
✓ Text alternatives for images
✓ Color is not the only visual means
✓ Audio control available

### Level AA Compliance
✓ Contrast ratio meets standards
✓ Text can be resized
✓ Focus visible
✓ Multiple navigation methods

### Level AAA Features
✓ Enhanced contrast in high-contrast mode
✓ No timing requirements
✓ Comprehensive keyboard support
✓ Clear focus indicators

---

## Use Cases

### Education
- Students with dyslexia or reading difficulties
- Language learners needing pronunciation support
- Visually impaired students accessing course materials

### Professional
- Document review while multitasking
- Accessibility compliance for organizations
- Legal document review with bookmarking

### Personal
- Reading books or articles hands-free
- Accessing scanned documents
- Language learning and practice

---

## Privacy & Security

- **No data transmission**: All processing happens locally in the browser
- **No server uploads**: PDFs never leave your device
- **No tracking**: No analytics or user tracking
- **No storage**: Files are not saved (unless you bookmark pages)

---

## Limitations & Known Issues

- **Voice recognition**: Best in Chrome/Edge; limited in Safari/Firefox
- **OCR accuracy**: Depends on scan quality; low-quality scans may have errors
- **File size**: Very large PDFs (500+ pages) may be slow
- **Mobile support**: Best on desktop; mobile has limited voice features
- **Internet required**: Initial load needs CDN access for libraries

---

## Future Enhancements

Potential features for future versions:
- [ ] Offline support with service workers
- [ ] Cloud storage integration
- [ ] PDF annotations and notes
- [ ] Multi-file session management
- [ ] Export reading notes
- [ ] Reading statistics dashboard
- [ ] Custom voice training
- [ ] Advanced OCR preprocessing

---

## Support & Feedback

For issues, suggestions, or contributions:
- Report bugs through your organization's issue tracking system
- Request features based on user needs
- Provide feedback on accessibility improvements

---

## Credits


**Core Technologies**:
- Mozilla PDF.js Team
- Tesseract.js Contributors
- Web Speech API (W3C Standard)
[Specify your license - MIT, Apache 2.0, GPL, or proprietary]

---

## Version History

**Version 1.0** (Current)
- Initial release with full PDF reading support
- Voice command integration
- OCR for scanned documents
- Multi-language support
- Complete accessibility features

---

**For more information or technical support, contact the EkStep Foundation development team.**
