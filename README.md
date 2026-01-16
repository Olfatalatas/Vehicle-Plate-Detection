# 🚗 Automatic Number Plate Recognition (ANPR) System

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-green.svg)](https://opencv.org/)
[![Tesseract](https://img.shields.io/badge/OCR-Tesseract-orange.svg)](https://github.com/tesseract-ocr/tesseract)

## 📌 Project Overview
Sistem **Automatic Number Plate Recognition (ANPR)** ini dikembangkan untuk mendeteksi dan mengekstraksi teks plat nomor kendaraan secara otomatis dari citra statis.

Proyek ini mendemonstrasikan penerapan teknik **Traditional Computer Vision** (Image Processing) yang digabungkan dengan **Optical Character Recognition (OCR)**. Pendekatan ini dipilih karena efisiensinya yang tinggi dan kebutuhan komputasi yang rendah dibandingkan metode Deep Learning yang berat, sehingga cocok untuk implementasi awal pada sistem parkir pintar atau kontrol akses gerbang.

## ⚙️ How It Works (The Pipeline)
Sistem ini bekerja melalui *pipeline* pemrosesan citra bertahap untuk memastikan akurasi deteksi:

1.  **Grayscale Conversion**: Mengubah citra input menjadi skala abu-abu untuk mengurangi kompleksitas warna.
2.  **Noise Reduction**: Menggunakan *Bilateral Filter* untuk menghaluskan citra namun tetap menjaga ketajaman tepi (edges).
3.  **Edge Detection**: Mengimplementasikan algoritma *Canny Edge Detection* untuk menemukan struktur garis pada kendaraan.
4.  **Contour Localization**: Mencari kontur tertutup dan memfilternya berdasarkan rasio aspek segiempat yang menyerupai plat nomor.
5.  **Masking & Cropping**: Mengisolasi area plat nomor dari background kendaraan.
6.  **Character Recognition**: Menggunakan **Tesseract OCR** untuk membaca karakter alfanumerik dari hasil crop.

## 📸 Results Preview

<img width="258" height="216" alt="image" src="https://github.com/user-attachments/assets/9d975489-e761-4cff-bbbc-71a1772c3e6f" /> <img width="258" height="122" alt="image" src="https://github.com/user-attachments/assets/5948b62b-3197-4883-8f8c-4a9691a6e0a6" /> <img width="190" height="18" alt="image" src="https://github.com/user-attachments/assets/65913d98-02a7-42ce-b5f9-c8934a66f75f" />





**Accuracy Note:** Sistem bekerja optimal pada kondisi pencahayaan cukup dan sudut pengambilan gambar yang tegak lurus.

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Computer Vision:** OpenCV (`cv2`), Imutils
* **OCR Engine:** PyTesseract (Google Tesseract-OCR Engine)
* **Data Manipulation:** NumPy, Pandas
* **Visualization:** Matplotlib

## 🚀 How to Run
Jika Anda ingin mencoba menjalankan kode ini di mesin lokal:

1.  **Clone Repository**
    ```bash
    git clone [https://github.com/Olfatalatas/Vehicle-Plate-Detection.git](https://github.com/Olfatalatas/Vehicle-Plate-Detection.git)
    cd Vehicle-Plate-Detection
    ```

2.  **Install Dependencies**
    Pastikan Python sudah terinstall, lalu jalankan:
    ```bash
    pip install opencv-python imutils pytesseract matplotlib numpy
    ```
    *(Note: Anda juga perlu menginstall [Tesseract-OCR executable](https://github.com/UB-Mannheim/tesseract/wiki) di sistem operasi Anda).*

3.  **Run the Notebook**
    Buka file `PlatNomor.ipynb` menggunakan Jupyter Notebook atau VS Code dan jalankan setiap sel secara berurutan.

## 👤 Author
**Olfat Harits Alatas**
* **Role:** AI & Computer Vision Engineer
* **Specialization:** Embedded AI, Deep Learning, Image Processing
* Connect with me on [LinkedIn](https://www.linkedin.com/in/olfat-harits-alatas-ba626722b)

---
*⭐️ Star this repo if you find it useful!*
