# 🐾 Klasifikasi Suara Hewan Tiruan dengan CNN

Proyek ini menggunakan **Convolutional Neural Network (CNN)** untuk mengklasifikasikan **suara hewan yang ditirukan manusia** ke dalam 5 kategori:

- 🐄 Cow – "moo"
- 🐈 Cat – "meow"
- 🐕 Dog – "woof"
- 🐐 Goat – "mbee"
- 🐦 Bird – "tweet"

## 📁 Struktur Direktori

```
speech_classification/
├── dataset/
│   ├── cow/
│   ├── cat/
│   ├── dog/
│   ├── goat/
│   └── bird/
├── animal_sound_classification.ipynb
└── README.md
```

## 📦 Dataset

Dataset terdiri dari file `.wav` pendek (1–2 detik) berisi suara manusia yang menirukan suara hewan. Setiap kelas memiliki ~5 file simulasi (bisa diperbanyak).

## 🔍 Ekstraksi Fitur

Menggunakan **Mel Spectrogram** dengan `librosa`, karena lebih sesuai dengan cara telinga manusia memproses suara.

## 🧠 Model CNN

Model CNN terdiri dari:
- 2 Conv2D layer
- 2 MaxPooling2D
- 1 Dense + Dropout
- Softmax output layer (5 kelas)

## 🏋️ Pelatihan

Model dilatih selama 20 epoch dengan `categorical_crossentropy` dan `Adam optimizer`.

## 📈 Hasil

Akurasi training dan validasi divisualisasikan dalam grafik untuk memantau overfitting.

## 🚀 Cara Menjalankan

1. Clone repositori ini:
```
git clone https://github.com/username/speech_classification.git
```

2. Install dependensi:
```
pip install librosa tensorflow matplotlib numpy
```

3. Jalankan notebook:
```
jupyter notebook animal_sound_classification.ipynb
```

## 🙋‍♀️ Penulis

Proyek oleh Muhammad Rahmad. Dibuat untuk tugas klasifikasi suara berbasis CNN.
