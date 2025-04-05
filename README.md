
# Drowsiness Detection via Webcam on Google Colab

![main_thumb](https://github.com/user-attachments/assets/a31708f3-fe9c-4a73-9682-bb2b71764ffe)

![image](https://github.com/user-attachments/assets/26bf587b-cfcd-4bb7-bebb-d78580ab44bf)
![image](https://github.com/user-attachments/assets/47fe121d-f93b-4902-b543-4f1bf17fd674)

Deteksi kondisi mengantuk secara real-time menggunakan webcam langsung dari browser (via Google Colab) berbasis landmark wajah dan perhitungan **EAR (Eye Aspect Ratio)**.


## Metode Deteksi Mengantuk
Menggunakan **EAR (Eye Aspect Ratio)** berdasarkan landmark mata. Jika nilai EAR turun di bawah ambang batas 0.27, dianggap sebagai tanda mengantuk.

**Rumus EAR:**
```
EAR = (||p2 - p6|| + ||p3 - p5||) / (2 * ||p1 - p4||)
```

## Tools & Library
- Python 3 (via Google Colab)
- OpenCV
- Dlib
- NumPy
- JavaScript (untuk akses webcam dari browser)

## Cara Jalankan

1. **Clone atau Fork repo ini**
2. **Buka file Colab notebook**
3. **Jalankan semua cell** sesuai urutan
4. **Izinkan akses kamera di browser**
5. Tunggu hasil deteksi tiap 3 detik, akan muncul EAR dan visualisasi titik wajah

## Struktur Proyek
```
.
├── drowsiness.ipynb   # Notebook utama
├── shape_predictor_68_face_landmarks.dat  # Model landmark wajah
└── README.md                   # Dokumentasi ini
```

## Threshold EAR
Nilai default ambang batas:
```python
EAR_THRESHOLD = 0.27
```
Silakan disesuaikan sesuai keperluan atau tuning dataset.

## Resources
- [dlib shape predictor](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2)
- [Research paper: Real-Time Eye Blink Detection using Facial Landmarks](https://vision.fe.uni-lj.si/cvww2016/proceedings/papers/05.pdf)

## Author
Made with 💻 and ☕ by [@fliw](https://github.com/fliw)  
