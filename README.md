# Mojibake Cipher

> A seed-based reversible mojibake cipher that transforms text into garbled characters and restores it with the same seed.

![License](https://img.shields.io/badge/License-MIT-green)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow)
![Status](https://img.shields.io/badge/Status-Stable-brightgreen)

## ✨ Features

- 🔒 **Reversible encryption & decryption**
  - Restore the original text perfectly using the same seed.

- 🎲 **Seed-based transformation**
  - Every seed produces a unique result.
  - Identical text + identical seed = identical output.

- 🌏 **Unicode-safe encoding**
  - Uses a custom Unicode mapping instead of conventional binary output.
  - Produces visually "garbled" text while remaining fully reversible.

- ⚡ **No dependencies**
  - Pure HTML, CSS, and JavaScript.
  - Runs entirely in your browser.

- 🔍 **Processing visualization**
  - View every transformation step:
    - UTF-8 bytes
    - PRNG bytes
    - XOR bytes
    - Character mapping

- 🌐 **Multi-language UI**
  - English
  - Japanese
  - Chinese

---

## 📖 How It Works

```
Input Text
      │
      ▼
 UTF-8 Encoding
      │
      ▼
Seed → PRNG
      │
      ▼
      XOR
      │
      ▼
Custom Unicode Mapping
      │
      ▼
Garbled Text
```

To restore the original text, simply perform the reverse process using the **same seed**.

---

## 🚀 Usage

1. Enter the text.
2. Enter any seed.
3. Click **Scramble**.
4. Share or save the generated garbled text.
5. To restore it, switch to **Restore**, paste the garbled text, and enter the **same seed**.

---

## 🛠️ Algorithm

1. Convert the input into UTF-8 bytes.
2. Generate a deterministic PRNG stream from the seed.
3. XOR every byte with the PRNG output.
4. Pack bytes into 16-bit values.
5. Map each value to a unique Unicode character.
6. Reverse the process for restoration.

This transformation is **fully reversible**, provided the original seed is used.

---

## 📷 Preview

<img width="100%" alt="preview" src="preview.png">

---

## 📄 License

MIT License
