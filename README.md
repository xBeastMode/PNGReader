# 🖼️ PNGReader (Work in Progress)

A minimal PNG file reader written in modern C++, built as a learning project to explore binary file formats, compression, and image decoding.

> ⚠️ **Status:** Work in progress — incomplete implementation, currently focused on core parsing

---

## 🧠 Overview

PNGReader is an experimental project aimed at understanding the internal structure of PNG files by implementing a decoder from scratch.

Rather than relying on existing libraries, this project focuses on manually parsing:

- PNG file structure and signature  
- Chunk-based format (IHDR, IDAT, IEND, etc.)  
- Binary data handling and endianness  
- Scanline processing  

---

## ✨ Current Features

- ✅ PNG file signature validation  
- ✅ Basic chunk parsing  
- ✅ IHDR (image header) extraction  
- ⚠️ Partial support for IDAT data handling  
- ❌ Scanline reconstruction (in progress)  
- ❌ Full image decoding  

---

## 🧩 What Makes PNG Complex?

PNG is deceptively simple but involves several non-trivial concepts:

- Chunk-based file structure  
- DEFLATE compression (zlib)  
- Filtered scanlines (Sub, Up, Average, Paeth)  
- Byte-level data reconstruction  
- CRC validation  

This project focuses on understanding and implementing these pieces step by step.

---

## 🚧 Current Limitations

- Incomplete IDAT decoding  
- No full image reconstruction yet  
- Limited support for PNG variants  
- No rendering/output (raw decoding only)  

---

## 🛣️ Roadmap

- Implement full IDAT decompression  
- Add scanline filter reconstruction  
- Support basic image output (e.g. raw buffer or PPM)  
- Add CRC validation  
- Improve error handling  

---

## 🧪 Learning Outcomes

This project demonstrates:

- Binary file parsing in C++  
- Working with byte streams and buffers  
- Understanding compression formats (zlib/DEFLATE)  
- Handling structured file formats  
- Debugging low-level data transformations  

---

## 🧠 Why This Project?

PNG decoding is a well-known “hard but educational” problem in systems programming.

This project was built to:

- Deepen understanding of file formats  
- Practice low-level data handling  
- Explore how real-world encoders/decoders work  

---

## 📦 Build

```bash
cmake -S . -B build
cmake --build build
```

---

## ▶️ Run

```bash
./build/PNGReader <image.png>
```

---

## 💡 Note

This is an educational project and not intended to replace production-ready image libraries.
