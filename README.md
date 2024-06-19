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
