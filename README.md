# 💳 Machine Readable Card Formatter

A sleek, browser-based credit card visualization tool that generates realistic card mockups from structured data. Built with vanilla HTML, CSS, and JavaScript — no dependencies required.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)

## ✨ Features

- **ISO/IEC 7810 ID-1 Compliant** — Standard credit card dimensions (85.60mm × 53.98mm ratio)
- **OCR-A Typography** — Machine-readable font styling for authentic appearance
- **Dynamic Card Detection** — Auto-detects Visa, Mastercard, Amex, Discover, Diners Club, and JCB
- **Responsive Font Sizing** — Card numbers scale automatically based on digit count (13-19 digits)
- **Gradient Designs** — Modern holographic-style card backgrounds
- **Batch Processing** — Generate multiple cards from multi-line input
- **Mobile Responsive** — Adapts to any screen size
- **Zero Dependencies** — Pure HTML/CSS/JS, runs anywhere

## 🚀 Quick Start

1. **Download** the HTML file
2. **Open** in any modern browser (Chrome, Firefox, Safari, Edge)
3. **Enter** card data in the format: `NAME|CARDNUMBER|MM|YYYY|CVV`
4. **Click** "Generate Cards"

### Example Input
John Doe|4532123456789012|12|2027|123 Jane Smith|5555123456789012|06|2026|456 Bob Wilson|378212345678901|09|2028|1234

## 📋 Input Format

| Field | Description | Example |
|-------|-------------|---------|
| `NAME` | Cardholder name (uppercase) | `JOHN DOE` |
| `CARDNUMBER` | 13-19 digit PAN | `4532123456789012` |
| `MM` | Expiration month (1-12) | `12` |
| `YYYY` | Expiration year (4 digits) | `2027` |
| `CVV` | Security code (3-4 digits) | `123` |

**Delimiter:** Pipe character `|`

**One card per line**

## 🎨 Card Design

- **Chip:** EMV-style gold contact chip
- **MRZ Zone:** Machine-readable zone with OCR-A typography
- **Holographic Gradient:** Purple-to-pink gradient with overlay patterns
- **Shadow & Depth:** Multi-layer box shadows for 3D effect
- **Glassmorphism:** Frosted glass effect on data panel

## 🛠️ Technical Details

### Supported Card Types
| Type | Pattern | Digits |
|------|---------|--------|
| Visa | `4...` | 13, 16, 19 |
| Mastercard | `51-55...` | 16 |
| Amex | `34, 37...` | 15 |
| Discover | `6011, 65...` | 16, 19 |
| Diners Club | `300-305, 36, 38...` | 14 |
| JCB | `35...` | 16-19 |

### Font Scaling Logic
Card numbers dynamically resize based on formatted length to ensure optimal readability:

| Formatted Length | Font Size | Letter Spacing |
|------------------|-----------|----------------|
| ≤15 chars | 26px | 4px |
| 16 chars | 24px | 3.5px |
| 17 chars | 22px | 3px |
| 18 chars | 21px | 2.8px |
| 19 chars | 20px | 2.5px |
| 20 chars | 19px | 2.3px |
| 21 chars | 18px | 2px |
| 22 chars | 17px | 1.8px |
| 23 chars | 16px | 1.6px |

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl + Enter` | Generate cards |
| `Tab` | Navigate between fields |

## 🌐 Browser Support

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

## ⚠️ Disclaimer

**This tool is for educational and visualization purposes only.**

- Does NOT validate card numbers using Luhn algorithm
- Does NOT verify card authenticity
- Does NOT store or transmit data
- All processing happens client-side in your browser

**Never use real, active payment card data.** This is a mockup generator for design, testing, and educational purposes.

## 📄 License

MIT License — feel free to use, modify, and distribute.

## 🙏 Credits

- Fonts: System fonts with OCR-A fallbacks
- Design inspired by ISO/IEC 7810 ID-1 standard
- Gradient palette: [uigradients.com](https://uigradients.com)

---


