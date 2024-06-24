# Menjadi-Google-Cloud-Architect-Submission

# submission 1 : 
Menjalankan Dockerfile di cloud shell
```cmd
docker build -t testapp:0.1 .
docker images
docker run -p 4000:8000 --name my-test-app testapp:0.1 # (8000 port expose app di Docker -> mapping ke 4000)
```

Buat Artifact Registry dan Autentikasi dengan Artifact Registry
```cmd
gcloud artifacts repositories create backend --repository-format=docker --location=asia-southeast2 --async
gcloud auth configure-docker asia-southeast2-docker.pkg.dev
```

Build dan Push Docker Image
```cmd
docker build -t asia-southeast2-docker.pkg.dev/${GOOGLE_CLOUD_PROJECT}/backend/notes-app:latest .
docker push asia-southeast2-docker.pkg.dev/${GOOGLE_CLOUD_PROJECT}/backend/notes-app:latest
```

Lanjut Deploy ke Google Kubernetes Engine dengan Cloud Console 🗿

# submission 2 (proyek akhir) : 
### Kriteria 1: Membuat Diagram Rancangan Arsitektur Cloud
<img src="https://github.com/indrayyana/Menjadi-Google-Cloud-Architect-Submission/blob/main/img/kriteria%201.png">

### Kriteria 2 & 3 `(private) 🗿`

### Kriteria 4: Membuat Custom Dashboard untuk Pemantauan
<img src="https://github.com/indrayyana/Menjadi-Google-Cloud-Architect-Submission/blob/main/img/kriteria%204.1.jpeg">
<img src="https://github.com/indrayyana/Menjadi-Google-Cloud-Architect-Submission/blob/main/img/kriteria%204.2.jpeg">

### Kriteria 5: Memberi Hak Akses ke Auditor Eksternal
Beri hak akses ke Reviewer Dicoding dengan menggunakan Cloud IAM & Admin

### Kriteria 6: Menghitung Biaya Arsitektur Cloud
<img src="https://github.com/indrayyana/Menjadi-Google-Cloud-Architect-Submission/blob/main/img/kriteria%206.1.jpeg">
<img src="https://github.com/indrayyana/Menjadi-Google-Cloud-Architect-Submission/blob/main/img/kriteria%206.2.jpeg">
<img src="https://github.com/indrayyana/Menjadi-Google-Cloud-Architect-Submission/blob/main/img/kriteria%206.3.jpeg">




